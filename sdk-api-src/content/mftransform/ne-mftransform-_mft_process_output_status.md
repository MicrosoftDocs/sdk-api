---
UID: NE:mftransform._MFT_PROCESS_OUTPUT_STATUS
title: "_MFT_PROCESS_OUTPUT_STATUS"
author: windows-sdk-content
description: Indicates the status of a call to IMFTransform::ProcessOutput.
old-location: mf\_mft_process_output_status.htm
old-project: medfound
ms.assetid: 80804b33-1dac-41f8-8446-8f929bf9b931
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 80804b33-1dac-41f8-8446-8f929bf9b931, MFT_PROCESS_OUTPUT_STATUS_NEW_STREAMS, _MFT_PROCESS_OUTPUT_STATUS, _MFT_PROCESS_OUTPUT_STATUS enumeration [Media Foundation], mf._mft_process_output_status, mftransform/MFT_PROCESS_OUTPUT_STATUS_NEW_STREAMS, mftransform/_MFT_PROCESS_OUTPUT_STATUS
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mftransform.h
api_name:
 - _MFT_PROCESS_OUTPUT_STATUS
product: Windows
targetos: Windows
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFT_PROCESS_OUTPUT_STATUS enumeration


## -description



Indicates the status of a call to <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a>.




## -enum-fields




### -field MFT_PROCESS_OUTPUT_STATUS_NEW_STREAMS

The Media Foundation transform (MFT) has created one or more new output streams.


## -remarks



If the MFT sets this flag, the <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> method returns MF_E_TRANSFORM_STREAM_CHANGE and no output data is produced. The client should respond as follows:

<ol>
<li>
Call <a href="https://msdn.microsoft.com/491f7f44-fcac-4236-ba5c-e5705267c6c2">IMFTransform::GetStreamCount</a> to get the new number of streams.

</li>
<li>
Call <a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">IMFTransform::GetStreamIDs</a> to get the new stream identifiers.

</li>
<li>
Call <a href="https://msdn.microsoft.com/d0f75414-18cf-4e76-b875-5f373510c87b">IMFTransform::GetOutputAvailableType</a> and <a href="https://msdn.microsoft.com/a9a1d03f-2e56-490c-885b-78c69dea8e92">IMFTransform::SetOutputType</a> to set the media types on the new streams.

</li>
</ol>
Until these steps are completed, all further calls to <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> return MF_E_TRANSFORM_STREAM_CHANGE.




## -see-also




<a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

