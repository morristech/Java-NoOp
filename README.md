Java - NoOp
===========
This is probably one of the simplest Java annotation processing libraries out there.
It generates [no-op implementations](https://en.wikipedia.org/wiki/NOP) of your interfaces. 

Usage
-----
* Simply annotate your interface with `@NoOp` like this:

```java
@NoOp
public interface TestInterface {

    byte aByte();
    Byte aByteObject();

    short aShort();
    Short aShortObject();

    int anInt();
    Integer anIntObject();

    long aLong();
    Long aLongObject();

    float aFloat();
    Float aFloatObject();

    double aDouble();
    Double aDoubleObject();

    char aChar();
    Character aCharObject();

    boolean aBoolean();
    Boolean aBooleanObject();

    void aVoid();
}
```

* And it will generate the following no-op implementation at compile time:

```java
public class NoOpTestInterface implements TestInterface {

  @Override
  public byte aByte() {
    return (byte) 0;
  }

  @Override
  public Byte aByteObject() {
    return null;
  }

  @Override
  public short aShort() {
    return (short) 0;
  }

  @Override
  public Short aShortObject() {
    return null;
  }

  @Override
  public int anInt() {
    return 0;
  }

  @Override
  public Integer anIntObject() {
    return null;
  }

  @Override
  public long aLong() {
    return 0L;
  }

  @Override
  public Long aLongObject() {
    return null;
  }

  @Override
  public float aFloat() {
    return 0.0F;
  }

  @Override
  public Float aFloatObject() {
    return null;
  }

  @Override
  public double aDouble() {
    return 0.0D;
  }

  @Override
  public Double aDoubleObject() {
    return null;
  }

  @Override
  public char aChar() {
    return ' ';
  }

  @Override
  public Character aCharObject() {
    return null;
  }

  @Override
  public boolean aBoolean() {
    return false;
  }

  @Override
  public Boolean aBooleanObject() {
    return null;
  }

  @Override
  public void aVoid() {
  }
}
```

Download
--------

*- coming soon -*

License
-------
This project is licensed under the [MIT License](https://raw.githubusercontent.com/jenzz/Java-NoOp/master/LICENSE).