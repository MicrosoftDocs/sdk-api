---
UID: NF:mfmediaengine.IMFExtendedDRMTypeSupport.IsTypeSupportedEx
tech.root: mf
title: IMFExtendedDRMTypeSupport::IsTypeSupportedEx
ms.date: 04/06/2022
targetos: Windows
description: Queries wether the specified content type is supported for the specified key system.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfmediaengine.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFExtendedDRMTypeSupport::IsTypeSupportedEx
f1_keywords:
 - IMFExtendedDRMTypeSupport::IsTypeSupportedEx
 - mfmediaengine/IMFExtendedDRMTypeSupport::IsTypeSupportedEx
dev_langs:
 - c++
helpviewer_keywords:
 - IsTypeSupportedEx
---

## -description

Queries whether the specified content type is supported for the specified key system.

## -parameters

### -param type [in]

A **BSTR** identifying the features for which support is queried. This parameter accepts RFC 2045 Content-Type strings to specify media type and subtype identifiers, and RFC 6381 Codecs identifiers for the codecs required. These base strings are consistent with those used in the HTML5 HTMLMediaElement canPlayType method. RFC 2045 allows for additional, custom parameters as modifiers in the form of ";&lt;parameter&gt;=&lt;name&gt;\[=&lt;value&gt;\] \[,&lt;name&gt;\[=&lt;value&gt;\]". RFC 2045 compliant parsers must ignore these parameters if not recognized. For the feature queries, &lt;parameter&gt; is named feature.

The implementation requires the RFC 2045 media type and subtype identifiers, for example "video/mp4", and RFC 6381 codec parameter codec=”&lt;video codec&gt;\[,&lt;audio codec&gt;\]” to always be present in order to provide valid query results.

Note that the terms content type and type are well known historically as MIME type.

### -param keySystem [in]

A **BSTR** identifying the PlayReady namespace to check query against, specifying hardware or software protection. Use "com.microsoft.playready.recommendation.3000" for hardware queries (PlayReady must have support for hardware offload), "com.microsoft.playready.recommendation.2000" for explicitly querying for software protection support, and "com.microsoft.playready.recommendation" for general queries (must answer for software protection support to guarantee backward compatibility).

### -param pAnswer [out]

A value from the [MF_MEDIA_ENGINE_CANPLAY](ne-mfmediaengine-mf_media_engine_canplay) enumeration indicating if the queried capabilities are likely supported, are possibly supported, or are unsupported.



## -returns

S_OK on success.

## -remarks
The *type* input parameter must have RFC 6381 Content-Type media type and subtype identifiers present.  It must also have the RFC 2045 Codecs parameter string present.  MPEG-4 is the only container supported for this API.  H.264 (avc1) and HEVC (hvc1, hev1) are the only video codecs providing supported answers.  MPEG-4 (mp4a), MPEG-1 Layer 3 (mp3), Dolby Digital (ac-3), and Dolby Digital Plus (ec-3) are the only audio codecs providing supported answers.  Supported strings are:

`video/mp4;codecs=”avc1,<audio codec>”`

`video/mp4;codecs=”hvc1, <audio codec>”`

`video/mp4;codecs=”hev1, <audio codec>”`

Starting with the Windows 10, version 1709, the following are also supported:

`Video/mp4;codecs=”vp9,<audio codec>”`

`Video/mp4;codecs=”vp09,<audio codec>”`

The features part of the query string is appended to one the above strings using a semicolon delimiter. The underlying graphics driver and hardware impose constraints on how features may be queried.  For the video subsystems the following requirements apply:

1.	Only one query of feature names plus values may be used from each of the subsystems in a single call
2.	A Decode subsystem query may be performed without a Display 1, Display 2, or Output Protection query
3.	A Display 1 subsystem query requires a Decode subsystem query to be present
4.	A Display 2 subsystem query requires a Decode subsystem query, but does not require a Display 1 subsystem query.
5.	An output protection subsystem (HDCP) query may be performed with or without a Decode, Display 1, or Display 2 subsystem query, subject to constraints #3 and #4.

The `General: Efficiency` query may be combined with any other subsystem queries.

The returned result is the logical AND of all individual feature queries, with the following clarification:  A **Maybe** result is only allowed from the output protection subsystem, and only temporarily.  This **Maybe** takes precedence over a **Probably** result from the AND of all other feature queries, until the **Maybe** resolves over time to either **Probably** or **Not Supported**.  The current time limit for **Maybe** to resolve is 10 seconds.

The following table lists the supported individual feature queries, organized by video subsystem:


|Item  |Video Sub-system  |Feature Name  |Feature Value |Description |Mandatory for this subsystem |
|---------|---------|---------|---------|---------|---------|
|1a     |Decode   |decode-res-x         |Non-negative number in pixels         |Does the video decoder support this maximum resolution in the X-axis?         |Y       |
|1b     |Decode   |decode-res-y         |Non-negative number in pixels         |Does the video decoder support this maximum resolution in the Y-axis?         |Y       |
|1c     |Decode   |decode-bitrate         |Positive number in kilobits per second (Kbps)         |Does the video decoder support this maximum bitrate?         |Y       |
|1d     |Decode   |decode-fps         |24, 25, 29.97, 30, 50, 59.94, or 60         |Does the video decoded support this maximum frames per second (FPS) value?         |Y       |
|1e     |Decode   |decode-bpc (decode-bpp is deprecated)         |0, 8, 10, or 12         |Can the video decoder consume this per-pixel color depth?         |Y       |
|1f     |Decode   |decoder-hardware-acceleration<sup>**</sup>         |1 or no value as true         |Is DXVA hardware acceleration available regardless of an OS decoder being present?         |N       |
|1g     |Decode   |decoder-software-acceleration <sup>**</sup>         |1 or no value as true         |Is an OS decoder present capable of decoding the stream?         |N       |
|1h     |Decode   |decoder-software-requires-hardware<sup>**</sup>         |1 or no value as true         |Does the OS decoder’s functionality require that DXVA hardware acceleration is present?         |N       |
|2a     |Display 1|display-res-x         |Non-negative number in pixels         |Does at least one intersecting<sup>**</sup> display support this resolution in the X-axis?         |Y       |
|2b     |Display 1|display-res-y         |Non-negative number in pixels         |Does at least one intersecting<sup>***</sup> display support this resolution in the Y-axis?         |Y       |
|2c     |Display 1|display-refreshrate         |24, 25, 29.97, 30, 50, 59.94, or 60         |Is the display configured (as understood by Windows) for at least the requested refresh rate?         |N       |
|2d     |Display 1|display-bpc (display-bpp is deprecated)         |8 or 10         |Do all intersecting displays with ≥ required resolution realize at least this color depth?         |N       |
|3     |Display 2<sup>*</sup>|hdr         |1 (supported)         |Does the target support High Dynamic Range (HDR) rendering         |Y       |
|4     |Output Protection|hdcp         |0 (off), 1 (on without HDCP 2.2 Type 1 restriction), 2 (on with HDCP 2.2 Type 1 restriction         |Do all intersecting enabled displays support at least the request protection level?         |Y       |
|5     |General: Efficiency<sup>**</sup>|efficiency-setting         |0 (off = no restriction), 1 (on = limit resolution when on battery power)         |Does the user want battery life, streaming overhead, and/or download speed in preference to highest resolution?<sup>****</sup>         |Y       |
|6a     |Decryption|encryption-type         |“cenc” or “cbcs”, with optional "-clearlead" suffix. |Is this encryption type supported for decryption with the specified codec / key-system? If value is unspecified, default value of "cenc" is used. Starting with Windows 11 Build 22621 and Windows 10 Build 19045.5796 or later, the suffix "-clearlead" is supported. When "-clearlead" is appended to the encryption type value, support for using clear content at the very beginning of encrypted content is also requested. Clear content at the beginning of the content speeds up the time to presenting the first frame. If "-clearlead" is added to the encryption-type, the version number of the requested codec will be checked. The AV1 and VP9 codecs will be checked for major version 2, and HEVC will be checked for v2.0.53421 or greater.       |N       |
|6b     |Decryption|encryption-iv-size         |8 or 16 |Is this Initialization Vector (IV) size (in bytes) supported for decryption with the specified codec / key-system? If value is unspecified, default value of 8 is used.        |N       |

<sup>*</sup> Only supported on Windows 10, version 1607 and newer OS versions

<sup>**</sup> Only supported on Windows 10, version 1709 and newer OS versions

<sup>***</sup> The intersection algorithm is:
1. Find all displays where application user interface video client region has pixels.
2. Find all graphics adapters driving the displays from step 1.  For a hardware DRM query, this set of adapters is filtered to only those adapters having hardware DRM support.
3. Find all displays connected to the graphics adapter(s) from step 2.

<sup>****</sup> It is up to the content provider to choose the resolution limit to use when this policy is on. A 1080p limit is recommended, but 720p may be used.  Note that the input for this policy comes from the Video Settings user interface page added in Windows 10, version 1709. 

The pairs for items 1a and 1b and 2a and 2b are each computed as (requested x >= actual intersecting set maximum x) AND (requested y >= actual intersecting set maximum y), with a modification that portrait display are normalized to landscape by swapping x and y as necessary.

The hdcp query (item 4) has a computationally expensive first invocation cost.  HDCP must be turned on at the requested level to probe whether the requested level can be met with the active display topology.  The **Maybe** result due to HDCP being evaluated asynchronously and taking up to several seconds with HDCP 2.2, but the query being synchronous with minimum blocking, requires that the caller use the query repeatedly until the result finalizes as **Probably** or **Not Supported**.  Changing the requested HDCP level in a query while still in the Maybe state will likely result in an invalid response.  The **Maybe** timeout is approximately 10 seconds.

It is strongly recommended not to invoke an hdcp query more often than once every 250 milliseconds, due to underlying computational cost.  500 milliseconds is the preferred minimum.  Caching is performed to minimize this cost, but any display topology changes while polling invalidate the caching.

As an implementation detail, graphics adapters may choose to use HDCP 2.2 if all nodes support it, even if the HDCP 2.2 Type 1 restriction has not been set.  HDCP 2.2 may take significantly longer than HDCP 1.x to engage.  Observations on current generation TVs show times up to 8 seconds, versus about 1 second for HDCP 1.x devices including repeaters.  Therefore, a first `hdcp=1` query on application startup or after an output topology change requires waiting up to 8 seconds plus margin for this worst case.   Using 10 seconds as a maximum wait, it is recommended to perform the application startup query when the user is least expected to pick a title, for example on an initial UI.  If no topology changes occur, all further hdcp queries will be sub-second.  If the content has the same HDCP output requirement as the query , the caching will eljminate the multi-second wait occurring again at playback start.  

On an output topology change, high-resolution TVs and monitors often take several seconds to stabilize the desktop.  A change, and especially reduction, in output protection level will usually cause active playback with hardware DRM to fail by design.  Here, a reaction to an **MF_POLICY_UNSUPPORTED** (0xC00D7159) error should be to hide the error from the user, requery, and resume with an appropriate content version for any changed capabilities.  Effectively, this acts as an extension of the “hotplug” stabilization time.

Software DRM decode feature queries are potentially ambiguous on performance as the H.264 implementation allows for either software decoding or DirectX Video Acceleration (DXVA) GPU offload.  However, H.264 DXVA is very common across all Windows endpoints.

A functional limitation with software DRM decode queries is that the decode-bpc is not evaluated.  Windows does not support H.264 10-bit decoding, but a query with `decode-bpc=10` will succeed.

The feature query result reflects the maximum theoretical capabilities of the subsystems.  Other activity in the GPU or varying power states may reduce actual capability.

### Hardware DRM query examples
The following shows the most common usage for 4K 10-bit HEVC Standard Dynamic Range (SDR) content with hardware DRM and HDCP 2.2 Type 1 restriction:

`IsTypeSupported(‘com.microsoft.playready.recommendation.3000’,’video/mp4;codecs=”hvc1,mp4a”;features=”decode-res-x=3840,decode-res-y=2160,decode-bitrate=20000,decode-fps=30,decode-bpc=10,display-res-x=3840,display-res-y=2160,display-bpc=8,hdcp=2”’);`

Where `mp4a` may be replaced with `mp3`, `ac-3`, or `ec-3`.  Decode-bitrate may be adjusted per the content provider’s encoding.  `decode-fps` may be set to 60 rather than 30 but may be gated by throughput capability of the hardware DRM security processor.  `display-res-x` and `display-res-y` values may be set lower than full 4K if the provider wishes to push 4K streams to 3200 x 1800, 3000 x 2000, or 2560 x 1440 displays, for example.

As decode query results aren’t expected to change dynamically, successive polling for `hdcp=2` while in Maybe can use a shorter form as a small optimization

`IsTypeSupported(‘com.microsoft.playready.recommendation.3000’,’video/mp4;codecs=”hvc1,mp4a”;features=”hdcp=2”’);`

Of course, this optimization won’t catch a dynamic monitor resolution change, but such a change would likely disrupt HDCP establishment in progress anyway.

The following shows the most common usage for 4K 10-bit HEVC High Dynamic Range (HDR) content with hardware DRM and HDCP 2.2 Type 1 restriction:

`IsTypeSupported(‘com.microsoft.playready.recommendation.3000’,’video/mp4;codecs=”hvc1,mp4a”;features=”decode-res-x=3840,decode-res-y=2160,decode-bitrate=20000,decode-fps=30,decode-bpc=10,display-res-x=3840,display-res-y=2160,display-bpc=8,hdr=1,hdcp=2”’);`

Note:  For Windows 10, version 1607, `hdr=1` indicates that either 10-bit MPO support with **DXGI_COLOR_SPACE_YCBCR_FULL_G22_LEFT_P2020** or **DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709** or **DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020** is present, or that the development-only HighColor registry key is present and has been set: `HKLM\SOFTWARE\Microsoft\Windows\DWM key HighColor` as a DWORD value of 1. 

The following shows the most common usage for 1080p 8-bit H.264 SDR content with hardware DRM and HDCP without 2.2 Type 1 restriction:

`IsTypeSupported(‘com.microsoft.playready.recommendation.3000’,’video/mp4;codecs=”avc1,mp4a”;features=”decode-res-x=1920,decode-res-y=1080,decode-bitrate=10000,decode-fps=30,decode-bpc=8,display-res-x=1920,display-res-y=1080,display-bpc=8,hdcp=1”’);`


## -see-also
[MF_MEDIA_ENGINE_CANPLAY](ne-mfmediaengine-mf_media_engine_canplay)


