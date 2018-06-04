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

# PBEGIN_RESTYPECALL_ROUTINE callback function


## -description


Starts a call to a resource control code. The <b>PBEGIN_RESTYPECALL_ROUTINE</b> type defines a pointer to this callback function.


## -parameters




### -param ResourceTypeName [in]

The name of the resource type.


### -param ControlCode [in]

The control code to call.


### -param InBuffer [in]

A pointer to the buffer that contains the input data for the call to the control code.


### -param InBufferSize [in]

The size of the buffer specified by <i>InBuffer</i>, in bytes.


### -param OutBuffer [out]

A pointer to the buffer that contains the output data for the call to the control code.


### -param OutBufferSize [in]

The size of the buffer specified by <i>OutBuffer</i>, in bytes.


### -param BytesReturned [out]

The size of the data returned by <i>OutBuffer</i>, in bytes.


### -param context [in]

The context to the resource type control code that was called.

<b>Windows Server 2012 R2:  </b>This parameter was added in Windows Server 2016.


### -param ReturnedAsynchronously [out]

<b>TRUE</b> if the operation returns asynchronously; otherwise, <b>FALSE</b>.

<b>Windows Server 2012 R2:  </b>This parameter was added in Windows Server 2016.


#### - resCallId [in]

This parameter was removed in Windows Server 2016.

<b>Windows Server 2012 R2:  </b>This parameter is only supported in Windows Server 2012 R2.


## -returns



The function returns one of the following values, or a system error code:




## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>



<a href="https://msdn.microsoft.com/a854829d-ed05-40a0-b7c8-c3e5ab888220">Resource Type Control Codes</a>
 

 

