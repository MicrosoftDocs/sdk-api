---
UID: NE:mftransform._MFT_PROCESS_OUTPUT_FLAGS
title: "_MFT_PROCESS_OUTPUT_FLAGS"
author: windows-sdk-content
description: Defines flags for processing output samples in a Media Foundation transform (MFT).
old-location: mf\_mft_process_output_flags.htm
tech.root: medfound
ms.assetid: 846e91a5-7cd8-4b58-9484-b9cb9af0bebf
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 846e91a5-7cd8-4b58-9484-b9cb9af0bebf, MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER, MFT_PROCESS_OUTPUT_REGENERATE_LAST_OUTPUT, _MFT_PROCESS_OUTPUT_FLAGS, _MFT_PROCESS_OUTPUT_FLAGS enumeration [Media Foundation], mf._mft_process_output_flags, mftransform/MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER, mftransform/MFT_PROCESS_OUTPUT_REGENERATE_LAST_OUTPUT, mftransform/_MFT_PROCESS_OUTPUT_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - mftransform.h
api_name:
 - _MFT_PROCESS_OUTPUT_FLAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _MFT_PROCESS_OUTPUT_FLAGS enumeration


## -description



Defines flags for processing output samples in a Media Foundation transform (MFT).




## -enum-fields




### -field MFT_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER

Do not produce output for streams in which the <b>pSample</b> member of the <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structure is <b>NULL</b>. This flag is not valid unless the MFT has marked the output stream with the MFT_OUTPUT_STREAM_DISCARDABLE or MFT_OUTPUT_STREAM_LAZY_READ flag. For more information, see <a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">IMFTransform::GetOutputStreamInfo</a>.


### -field MFT_PROCESS_OUTPUT_REGENERATE_LAST_OUTPUT

Regenerates the last output sample.

<b>Note</b> Requires Windows 8.


## -see-also




<a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

