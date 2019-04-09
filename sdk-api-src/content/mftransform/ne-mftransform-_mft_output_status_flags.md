---
UID: NE:mftransform._MFT_OUTPUT_STATUS_FLAGS
title: "_MFT_OUTPUT_STATUS_FLAGS" (mftransform.h)
author: windows-sdk-content
description: Indicates whether a Media Foundation transform (MFT) can produce output data.
old-location: mf\_mft_output_status_flags.htm
tech.root: medfound
ms.assetid: 951900b1-364e-4867-a1f8-50d485d13c77
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 951900b1-364e-4867-a1f8-50d485d13c77, MFT_OUTPUT_STATUS_SAMPLE_READY, _MFT_OUTPUT_STATUS_FLAGS, _MFT_OUTPUT_STATUS_FLAGS enumeration [Media Foundation], mf._mft_output_status_flags, mftransform/MFT_OUTPUT_STATUS_SAMPLE_READY, mftransform/_MFT_OUTPUT_STATUS_FLAGS
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
 - _MFT_OUTPUT_STATUS_FLAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _MFT_OUTPUT_STATUS_FLAGS enumeration


## -description



Indicates whether a Media Foundation transform (MFT) can produce output data.




## -enum-fields




### -field MFT_OUTPUT_STATUS_SAMPLE_READY

There is a sample available for at least one output stream. To retrieve the available output samples, call <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a>.


## -see-also




<a href="https://msdn.microsoft.com/3eb82f76-088b-4abc-9f3a-dfa5ecd1068d">IMFTransform::GetOutputStatus</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

