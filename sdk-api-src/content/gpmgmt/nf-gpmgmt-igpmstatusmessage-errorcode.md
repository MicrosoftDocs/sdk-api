---
UID: NF:gpmgmt.IGPMStatusMessage.ErrorCode
title: IGPMStatusMessage::ErrorCode
author: windows-sdk-content
description: Returns the error that occurred during the GPMC operation.
old-location: gpmc\igpmstatusmessage_errorcode.htm
tech.root: gpmc
ms.assetid: 87a50523-1acb-4b58-b867-ec19b0cf960a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ErrorCode, ErrorCode method [GPMC], ErrorCode method [GPMC],GPMStatusMessage class, ErrorCode method [GPMC],IGPMStatusMessage interface, GPMStatusMessage class [GPMC],ErrorCode method, IGPMStatusMessage interface [GPMC],ErrorCode method, IGPMStatusMessage.ErrorCode, IGPMStatusMessage::ErrorCode, _win32_igpmstatusmessage_errorcode, gpmc.igpmstatusmessage_errorcode, gpmgmt/IGPMStatusMessage::ErrorCode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMStatusMessage.ErrorCode
 - GPMStatusMessage.ErrorCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

