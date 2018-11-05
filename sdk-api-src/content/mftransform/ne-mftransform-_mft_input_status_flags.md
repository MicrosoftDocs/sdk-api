---
UID: NE:mftransform._MFT_INPUT_STATUS_FLAGS
title: "_MFT_INPUT_STATUS_FLAGS"
author: windows-sdk-content
description: Indicates the status of an input stream on a Media Foundation transform (MFT).
old-location: mf\_mft_input_status_flags.htm
tech.root: medfound
ms.assetid: c63052a1-58b6-4537-9214-6f8d79a9eafd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MFT_INPUT_STATUS_ACCEPT_DATA, _MFT_INPUT_STATUS_FLAGS, _MFT_INPUT_STATUS_FLAGS enumeration [Media Foundation], c63052a1-58b6-4537-9214-6f8d79a9eafd, mf._mft_input_status_flags, mftransform/MFT_INPUT_STATUS_ACCEPT_DATA, mftransform/_MFT_INPUT_STATUS_FLAGS
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
 - _MFT_INPUT_STATUS_FLAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _MFT_INPUT_STATUS_FLAGS enumeration


## -description



Indicates the status of an input stream on a Media Foundation transform (MFT).




## -enum-fields




### -field MFT_INPUT_STATUS_ACCEPT_DATA

The input stream can receive more data at this time. To deliver more input data, call <a href="https://msdn.microsoft.com/c94d406b-7cd9-42d4-ae9e-3d21dbb47209">IMFTransform::ProcessInput</a>.


## -see-also




<a href="https://msdn.microsoft.com/6205dc1a-f209-49aa-8632-837783ef5f04">IMFTransform::GetInputStatus</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

