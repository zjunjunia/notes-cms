---
title: CIE AS Computer Science - Chapter 1
date: '2018-06-28T00:05:00+03:00'
description: CIE AS Computer Science - Chapter 1
---
Information Representation
==========================

Number Representation
---------------------

-   **Denary:** normal integer numbers

-   **Binary**

    -   Values stored as a series of ones and zeroes

    -   A single 0 or 1 is called a binary digit or bit.

    -   Any group of 0s & 1s can represent a character

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|-----|----|----|----|---|---|---|---|
| 0   | 0  | 0  | 0  | 0 | 0 | 0 | 0 |

-   E.g. 65 in binary is 1000001

-   **BCD** (Binary Coded Decimal):

    -   Each digit in the number is written separately in a series of 4 bits

    -   E.g. 398 in BCD

    -   3 = 0011 9 = 1001 8 = 1000

    -   398 = 001110011000

    -   **Use of BCD:** used in business applications (arithmetic) where every
        digit has to be retained in a result

-   **Hexadecimal Numbers:**

    -   The base-16 number system (counting in 16)

    -   After 9, numbers represented by letters from A to F

| 256 | 16 | 1 |
|-----|----|---|
| 0   | 0  | 0 |

-   E.g. A5 in Denary = $$\left( 16 \times 10 \right) + \left( 1 \times 5
    \right) = 165$$

-   E.g. 65 in Hexadecimal = $$65 \div 16 = 4\ Remainder\ 1\therefore\  = 41$$ H

-   Quick way of translating hexadecimal to binary is by converting the
    hexadecimal to BCD

-   E.g. A5 in Binary: A = 1010 5 = 0101 A5 = 10100101

-   **Two’s Complement:**

    -   We can represent a negative number in binary by making the most
        significant bit (MSB) a sign bit, which will tell us whether the number
        is positive or negative.

| \-128 | 64 | 32 | 16 | 8 | 4 | 2 | 1   |
|-------|----|----|----|---|---|---|-----|
| MSB   | 0  | 0  | 0  | 0 | 0 | 0 | LSB |

-   Converting a negative denary number into binary Two’s Complement:

    -   Find the binary equivalent of the denary number

    -   Add an extra bit before the MSB and turn that into 0

    -   Flip all the bits: 0 to 1; 1 to 0

    -   Add 1

-   Converting Two’s Complement to denary:

    -   Flip all the bits: 0 to 1; 1 to 0

    -   Add 1

    -   Simple conversion from binary to denary (put a –ve)

Image Representation
--------------------

-   A **bitmapped image** is encoded by assigning a solid color to each pixel.

-   **Pixels** are small blocks of addressable areas and the color they have is
    represented by binary & stored as bits

-   A bitmapped image also contains a **file header** which are a few bytes of
    binary and represents basic information about the graphic, such as image
    resolution, size and number of colors.

-   **Image Resolution:** the amount of pixels an image contains per inch or per
    centimeter.

-   **Screen resolution:** the number of pixels per row by the number of pixels
    per column, e.g. HD is 720 by 1280 px

$$
Total\ Number\ of\ Pixels = Width \times Height
$$

-   **Color depth:** number of bits used to represent the color of a single
    pixel

    -   E.g. a 1 bit image can only store 21 pixels which equals to 2.
        Therefore, a 1 bit image is monochromatic

    -   An image with *n* bits has 2*n* colors per pixel

    -   The higher the color depth, the better color quality

    -   The higher the color depth, the larger the file size.

$$
File\ Size = Number\ of\ Pixels \times Colour\ Depth
$$

-   **Vector graphics**: images defined using mathematics & geometry i.e.
    points, lines, curves & shapes/polygon(s)

-   Objects and properties are stored mathematically.

-   **Drawing list:** set of commands used to define a vector

-   Vectors are scalable and do not pixelate like a bitmap image therefore are
    used by corporations to create logos as they can be resized without losing
    quality

-   Bitmapped images are used by general computer users as they are not big in
    file size and can be manipulated.

Sound
-----

-   Sound are vibrations that travel through a medium

-   Sound waves are continuous in nature, which means there is infinite amount
    of detail for a sound.

-   **Analogue to Digital Converter (ADC):** converts analogue sound into
    digital signals which can be digitally stored

-   **Digital to Analogue Converter (DAC)**: converts digital signals into
    analogue sound that can be output

-   An analogue sound wave is picked up by a microphone and sent to an ADC in
    the form of analogue electrical signals. Once the sound wave is converted
    into a digital form it can be stored and manipulated

-   Sound in analogue form can be represented by wave forms; the height of these
    waves can be **sampled** regularly with the height being represented by a
    bit-code

![https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcSeslr-izhN7Wo5fAKzMuw2A_l-6V22TnkYZBB56Z8v04aIdYIw](media/2b85db21fb5d221e09419989bed0a93a.jpg)

-   **Sampling Rate:** number of samples taken per second

-   A higher sampling rate means the waveform will be converted from analog to
    digital form more accurately.

-   **Sampling Resolution:** no. of bits assigned to each sample

-   The sampling resolution allows you to set the range of volumes storable for
    each sample

-   The quality of a sound produced using a sound sampler depends on the
    sampling rate and sampling resolution

-   Higher sampling rate/resolution means larger file size

-   **Bit Rate:** number of bits required to store 1sec of sound

$$
Bit\ Rate = Sampling\ Rate \times Sampling\ Resolution
$$

$$
File\ Size = Bit\ Rate \times Length\ of\ Sound
$$

-   **Lossless Compression:** type of compression that allows original data to
    be perfectly reconstructed from compression

    -   **Run-length encoding:** compression in which sequences with same data
        value in many consecutive values are stored as a single data value and
        count

    -   E.g. 00001234111111 can be written as (0-4)1234(1-6)

-   **Lossy Compression:** type of compression in which file accuracy is low,
    but file size is smaller than lossless

    -   **Perceptual coding:** works by reducing certain parts of a sound which
        are less audible to human hearing

Video
-----

-   **Frame Rate (FPS):** frequency at which frames in a video sequence are
    displayed

    -   Higher frame rate, better quality video = greater size

-   **Interlaced (e.g. 1080i):**

    -   Old Technology (70 years ago)

    -   Each field of a video image displays every other horizontal line of a
        complete image $$\therefore$$ doubles FPS

    -   Horizontal lines often visible to eye due to distortion

    -   **Pros:** Refreshes faster, better visual smoothness and saves bandwidth

    -   **Cons:** Becoming outdated and interlaced screen will not show fast
        moving objects clearly

-   **Progressive (e.g. 720p):**

    -   Excite every horizontal line simultaneously

    -   Thus frame rate is the same as the number of individual pictures in a
        video sequence

    -   This gives more detail in each frame

    -   **Pros:** Crisp, detailed frames and is new and popular

    -   **Con:** Rough frame transition

-   **Inter-frame compression:**

    -   Type of video compression and decreases file size

    -   It removes neighboring frames which are similar

    -   Some change in image data is redundant

    -   How redundant the change in image between frames is determines the
        amount of compression possible

-   **Temporal redundancy**: redundancy **between** frames

    -   This is the correlation between adjacent data points

    -   It is based upon abrupt transitions between frames

-   **Spatial redundancy:** redundancy **within** a frame

    -   An intercoded frame that is divided into macro blocks

    -   Blocks are not directly encoded with raw pixel values

    -   Encoder finds a block similar to the one in last frame

    -   This frame is the reference frame

    -   This process is done using algorithms

-   **Multimedia Container Formats:**

    -   Contains different types of data

    -   Can be audio or video or both codecs

    -   This interleaves the different type of data

    -   The video is compressed into codecs

    -   E.g. .avi, .mov, .mp4, .ogg, .rm

-   **Lossy Data Compression:**

    -   These programs eliminate unnecessary bits of data

    -   Reduces data file size more than lossless

    -   Unable to get back original version

-   **Lossless Data Compression:**

    -   Breaks data into smaller form of transmission

    -   Allows recreation of original
