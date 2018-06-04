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

# PRESOURCE_CONTROL_ROUTINE callback function


## -description


Performs an operation that applies to a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The 
    <b>PRESOURCE_CONTROL_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param Resource [in]

Resource identifier of the affected resource.


### -param ControlCode [in]


<a href="https://msdn.microsoft.com/b8ab57bd-f83e-46c2-9c9c-02107c3881bf">Control code</a> that represents the operation to be 
       performed. For a list of valid values for the <i>ControlCode</i> parameter, see 
       <a href="https://msdn.microsoft.com/a854829d-ed05-40a0-b7c8-c3e5ab888220">Resource Type Control Codes</a>.


### -param InBuffer [in, optional]

Pointer to a buffer containing data to be used in the operation. <i>InBuffer</i> can be 
       <b>NULL</b> if no data is required.


### -param InBufferSize [in]

Size, in bytes, of the buffer pointed to by <i>InBuffer</i>.


### -param OutBuffer [out, optional]

Pointer to a buffer containing data resulting from the operation. <i>OutBuffer</i> can be 
       <b>NULL</b> if the operation does not need to return data.


### -param OutBufferSize [in]

Size, in bytes, of the available space pointed to by <i>OutBuffer</i>.


### -param BytesReturned [out]

Actual size, in bytes, of the data resulting from the operation.


## -returns





Returns DWORD that ...






## -remarks



Some control codes should be handled by the resource DLL, while others should be left to the Resource Monitor. 
     For effective implementation strategies of the 
     <i>ResourceControl</i> entry-point function, see 
     <a href="https://msdn.microsoft.com/3aa4a591-b0ae-4f2f-8642-f524f7207397">Implementing ResourceControl</a>.


#### Examples

See <a href="mscs.resource_dll_examples">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

