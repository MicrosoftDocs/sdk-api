---
UID: NE:mfidl._MF_TRANSCODE_ADJUST_PROFILE_FLAGS
title: "_MF_TRANSCODE_ADJUST_PROFILE_FLAGS"
author: windows-sdk-content
description: Defines the profile flags that are set in the MF_TRANSCODE_ADJUST_PROFILE attribute.
old-location: mf\mf_transcode_adjust_profile_flags.htm
tech.root: medfound
ms.assetid: 65d7350f-a9d9-43c0-b3b6-c6169a727b4e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MF_TRANSCODE_ADJUST_PROFILE_DEFAULT, MF_TRANSCODE_ADJUST_PROFILE_FLAGS, MF_TRANSCODE_ADJUST_PROFILE_FLAGS enumeration [Media Foundation], MF_TRANSCODE_ADJUST_PROFILE_USE_SOURCE_ATTRIBUTES, _MF_TRANSCODE_ADJUST_PROFILE_FLAGS, mf.mf_transcode_adjust_profile_flags, mfidl/MF_TRANSCODE_ADJUST_PROFILE_DEFAULT, mfidl/MF_TRANSCODE_ADJUST_PROFILE_FLAGS, mfidl/MF_TRANSCODE_ADJUST_PROFILE_USE_SOURCE_ATTRIBUTES
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_TRANSCODE_ADJUST_PROFILE_FLAGS
product: Windows
targetos: Windows
req.typenames: MF_TRANSCODE_ADJUST_PROFILE_FLAGS
req.redist: 
---

# _MF_TRANSCODE_ADJUST_PROFILE_FLAGS enumeration


## -description


Defines the profile flags that are set in the <a href="https://msdn.microsoft.com/6782e080-284b-458d-8bc0-6e131a529e7b">MF_TRANSCODE_ADJUST_PROFILE</a> attribute.

These flags are checked by <a href="https://msdn.microsoft.com/ef3f19bf-1db9-459d-9617-d6cca9d6aba7">MFCreateTranscodeTopology</a> during topology building. Based on these flags, <b>MFCreateTranscodeTopology</b> adjusts the  transcode profile by modifying the configuration settings for the streams according to the input requirements of the encoder used in the topology. 

For more information about the stream settings that an application can specify, see <a href="https://msdn.microsoft.com/52b27359-b319-41a0-88e8-d23567420e92">Using the Transcode API</a>.


## -enum-fields




### -field MF_TRANSCODE_ADJUST_PROFILE_DEFAULT

Media Foundation uses the application-specified settings for audio and video streams. If the required settings are not provided by the application, the topology is created but the encoding session fails. For the video stream, the frame rate and the interlace mode settings are modified. For more information, see Remarks. 
 


### -field MF_TRANSCODE_ADJUST_PROFILE_USE_SOURCE_ATTRIBUTES

For both audio and video streams, the missing stream settings are filled by copying the input source attributes. This flag ensures the transcoded output file is the closest match to the input file.


## -remarks



If the <b>MF_TRANSCODE_ADJUST_PROFILE_DEFAULT</b> flag is specified, the following changes are made for the video stream:

<ul>
<li>If the frame rate of the media source specified in the <i>pSrc</i> parameter of  <a href="https://msdn.microsoft.com/ef3f19bf-1db9-459d-9617-d6cca9d6aba7">MFCreateTranscodeTopology</a> and the frame rate specified by the application in the <a href="https://msdn.microsoft.com/8336559c-06f1-478e-b921-e9eae7425230">MF_MT_FRAME_RATE</a> attribute differ by less than 1/1000, the profile uses the media source frame rate. This is because the pipeline considers the difference to be negligible.</li>
<li>If the application does not specify an interlaced mode by setting the <a href="https://msdn.microsoft.com/19aa0147-ac49-4a2e-ac75-e967fec9ca68">MF_MT_INTERLACE_MODE</a> attribute, the profile is changed to use progressive frames.</li>
</ul>
The <b>MF_TRANSCODE_ADJUST_PROFILE_DEFAULT</b> flag must be accompanied with the required audio and video stream attributes provided by the application. For the audio stream, the required attributes are as follows:

<ul>
<li>
<a href="https://msdn.microsoft.com/524283fb-d046-4f8c-a30f-4fe7ddb43174">MF_MT_AUDIO_NUM_CHANNELS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f640016d-595e-4b20-8ce8-23a029c2b064">MF_MT_AUDIO_SAMPLES_PER_SECOND</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7d304826-ad81-4243-a675-2f55b668b348">MF_MT_AUDIO_BLOCK_ALIGNMENT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0ee371fb-d980-44de-a9bd-201e2b72e874">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d78a8c4d-377e-45eb-9cf6-2d61b34e82d6">MF_MT_AUDIO_BITS_PER_SAMPLE</a>
</li>
</ul>
 For the video stream, the required attributes are as follows:

<ul>
<li>
<a href="https://msdn.microsoft.com/8336559c-06f1-478e-b921-e9eae7425230">MF_MT_FRAME_RATE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9f10a972-406f-47ef-b71c-86ed771c9a9a">MF_MT_FRAME_SIZE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cf9374a7-3688-4a6c-8339-d68c267c9bed">MF_MT_AVG_BITRATE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e82cdd22-7d3f-4858-befd-43fa6f9f915e">MF_MT_PIXEL_ASPECT_RATIO</a>
</li>
</ul>
  If these attributes are not set, <a href="https://msdn.microsoft.com/ef3f19bf-1db9-459d-9617-d6cca9d6aba7">MFCreateTranscodeTopology</a> creates the topology but Media Session fails to generate the encoded file. The failure code depends on the MFT node in the topology. For example, if the application does not set the frame size, the WMV encoder fails to encode the content and application gets the MF_E_INVALIDMEDIATYPE error code through the Media Session.  

Use the <b>MF_TRANSCODE_ADJUST_PROFILE_USE_SOURCE_ATTRIBUTES</b> flag when you want to transcode the file by using the input stream attributes. The input source stream attributes are copied to the output media type before the MFT node is inserted in the topology. If you set additional stream attributes, this flag does not overwrite the set values. Only the missing attributes are filled with the input source's attribute values. This flag is useful in remux scenario where you want to generate the output file in the same format as the input source. If you want to perform format conversion, make sure you set the <a href="https://msdn.microsoft.com/8e600943-92f1-4936-8c00-842fc7f4cb57">MF_MT_SUBTYPE</a>  attribute for the stream to specify the encoder that topology builder must use. The transform node is added in the topology unless <a href="https://msdn.microsoft.com/73f23aed-d1b9-4821-b1ca-0a07f02b6913">MF_TRANSCODE_DONOT_INSERT_ENCODER</a> is set. In this case, and the content is not encoded. Instead, if permitted by the container, the content is embedded in the specified container. 

For example, assume that your input source is an MP3 file.  You set the container to be <b>MFTranscodeContainerType_ASF</b>, you do not set any stream attributes, and you set the <b>MF_TRANSCODE_ADJUST_PROFILE_USE_SOURCE_ATTRIBUTES</b> flag. In this case, the generated output file is an ASF file (.wma)  containing MP3 media data. Note that if you use this flag, certain input stream attributes and the container type might not be compatible. 




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/24bf68a8-39bf-4302-b28c-71bb23b63469">Transcode API</a>
 

 

