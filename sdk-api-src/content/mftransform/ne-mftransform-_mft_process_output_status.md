---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

