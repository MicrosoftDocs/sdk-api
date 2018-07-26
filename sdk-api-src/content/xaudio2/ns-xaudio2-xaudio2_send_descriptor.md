---
UID: NS:xaudio2.XAUDIO2_SEND_DESCRIPTOR
title: XAUDIO2_SEND_DESCRIPTOR
author: windows-sdk-content
description: Defines a destination voice that is the target of a send from another voice and specifies whether a filter should be used.
old-location: xaudio2\xaudio2_send_descriptor.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_SEND_DESCRIPTOR
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: XAUDIO2_SEND_DESCRIPTOR, XAUDIO2_SEND_DESCRIPTOR structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_send_descriptor, xaudio2/XAUDIO2_SEND_DESCRIPTOR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XAUDIO2_SEND_DESCRIPTOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_SEND_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# XAUDIO2_SEND_DESCRIPTOR structure


## -description


Defines a destination voice that is the target of a send from another voice and specifies whether a filter should be used.


## -struct-fields




### -field Flags

Indicates whether a filter should be used on data sent to the voice pointed to by <b>pOutputVoice</b>. Flags can be 0 or XAUDIO2_SEND_USEFILTER.


### -field pOutputVoice

A pointer to an <a href="https://msdn.microsoft.com/library/Ee415917(v=VS.85).aspx">IXAudio2Voice</a> that will be the target of the send. The <b>pOutputVoice</b> member cannot be NULL.


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/40004128-4abb-4bcd-fe76-91276be8abec">How to: Change Voice Volume</a>



<a href="https://msdn.microsoft.com/76c1c138-4846-9c4f-7875-446867436ee9">How to: Use Submix Voices</a>



<a href="https://msdn.microsoft.com/library/Ee418607(v=VS.85).aspx">IXAudio2::CreateSourceVoice</a>



<a href="https://msdn.microsoft.com/library/Ee418608(v=VS.85).aspx">IXAudio2::CreateSubmixVoice</a>



<a href="https://msdn.microsoft.com/library/Ee418599(v=VS.85).aspx">IXAudio2Voice::SetOutputVoices</a>



<a href="https://msdn.microsoft.com/3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c">XAudio Structures</a>



<a href="https://msdn.microsoft.com/be34ce62-6552-45e2-a247-830ab55ea9ec">XAudio2 Sample Rate Conversions</a>
 

 

