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

# MI_Context_WriteCimError function


## -description


Sends a CIM (informative) error instance to the client.


## -parameters




### -param context [in]

Request context.


### -param error [in]

An instance of a <a href="https://msdn.microsoft.com/a7dc450d-7dbd-4097-a186-0e42f100fbfe">CIM_Error</a> class.


### -param flag [out]

<b>MI_TRUE</b> on return if the provider should continue execution. Otherwise, <b>MI_FALSE</b>.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



A provider calls this function to send a CIM error instance to the client.  This does not cancel the operation. Rather, this indicates the error to the client and gives the client the opportunity to determine if the operation should be continued or cancelled. It is then up to the provider to react accordingly.




## -see-also




<a href="https://msdn.microsoft.com/a7dc450d-7dbd-4097-a186-0e42f100fbfe">CIM_Error</a>



<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/96ef9e97-467b-4b71-a7f9-4f640102e744">MI_Context_PostCimError</a>



<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>
 

 

