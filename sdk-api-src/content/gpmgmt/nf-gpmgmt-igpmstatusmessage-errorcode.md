---
UID: NF:gpmgmt.IGPMStatusMessage.ErrorCode
title: IGPMStatusMessage::ErrorCode (gpmgmt.h)
description: Returns the error that occurred during the GPMC operation.
helpviewer_keywords: ["ErrorCode","ErrorCode method [GPMC]","ErrorCode method [GPMC]","GPMStatusMessage class","ErrorCode method [GPMC]","IGPMStatusMessage interface","GPMStatusMessage class [GPMC]","ErrorCode method","IGPMStatusMessage interface [GPMC]","ErrorCode method","IGPMStatusMessage.ErrorCode","IGPMStatusMessage::ErrorCode","_win32_igpmstatusmessage_errorcode","gpmc.igpmstatusmessage_errorcode","gpmgmt/IGPMStatusMessage::ErrorCode"]
old-location: gpmc\igpmstatusmessage_errorcode.htm
tech.root: gpmc
ms.assetid: 87a50523-1acb-4b58-b867-ec19b0cf960a
ms.date: 12/05/2018
ms.keywords: ErrorCode, ErrorCode method [GPMC], ErrorCode method [GPMC],GPMStatusMessage class, ErrorCode method [GPMC],IGPMStatusMessage interface, GPMStatusMessage class [GPMC],ErrorCode method, IGPMStatusMessage interface [GPMC],ErrorCode method, IGPMStatusMessage.ErrorCode, IGPMStatusMessage::ErrorCode, _win32_igpmstatusmessage_errorcode, gpmc.igpmstatusmessage_errorcode, gpmgmt/IGPMStatusMessage::ErrorCode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMStatusMessage::ErrorCode
 - gpmgmt/IGPMStatusMessage::ErrorCode
dev_langs:
 - c++
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
---

# IGPMStatusMessage::ErrorCode


## -description

Returns the error that occurred during the GPMC operation. If the operation was interacting with another system component, the error code is typically one returned by that component. Usually this is the first error GPMC hits while executing the operation. This error code is internally mapped to the operation error code returned by the <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstatusmessage-operationcode">OperationCode</a> method.

For example, if GPMC calls <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountsida">LookupAccountSid</a> while resolving the destination of a security group in a GPO import operation, and <b>LookupAccountSid</b> returns <b>E_ACCESSDENIED</b>, then the error code for the message will be <b>E_ACCESSDENIED</b> and the operation code of the message will be STATUS_ENTRY_DEST_UNRESOLVED.



## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmessage">IGPMStatusMessage</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>
