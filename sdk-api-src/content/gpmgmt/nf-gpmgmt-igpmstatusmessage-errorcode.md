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

# IGPMStatusMessage::ErrorCode


## -description


Returns the error that occurred during the GPMC operation. If the operation was interacting with another system component, the error code is typically one returned by that component. Usually this is the first error GPMC hits while executing the operation. This error code is internally mapped to the operation error code returned by the <a href="https://msdn.microsoft.com/f99dc90a-fabe-40fb-8289-36501a68b11d">OperationCode</a> method.

For example, if GPMC calls <a href="https://msdn.microsoft.com/b8a44ffc-86e1-4f79-ad51-8340da9eaefd">LookupAccountSid</a> while resolving the destination of a security group in a GPO import operation, and <b>LookupAccountSid</b> returns <b>E_ACCESSDENIED</b>, then the error code for the message will be <b>E_ACCESSDENIED</b> and the operation code of the message will be STATUS_ENTRY_DEST_UNRESOLVED.


## -parameters






## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/8570d40c-25c2-405c-b52a-dae6c0eb50e0">IGPMStatusMessage</a>



<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>
 

 

