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

# PSIGNAL_FAILURE_ROUTINE callback function


## -description


Reports that there was a failure in a resource instance. The <b>PSIGNAL_FAILURE_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param ResourceHandle [in]

A handle to the resource instance.


### -param FailureType [in]

A <a href="https://msdn.microsoft.com/C838BE66-5CAB-4884-AC64-EC5EC3A87679">FAILURE_TYPE</a> enumeration value that describes the failure type.

<b>Windows Server 2012:  </b>Not supported.


### -param ApplicationSpecificErrorCode [in]

An application error code.


#### - IsEmbeddedFailure [in]

Not supported.

<b>Windows Server 2012:  </b><b>TRUE</b> if this failure is an embedded failure; otherwise <b>FALSE</b>.


## -returns



Returns <b>ERROR_SUCCESS</b> (0), if the operation succeeds; otherwise returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>
 

 

