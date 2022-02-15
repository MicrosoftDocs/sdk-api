---
UID: NF:gpmgmt.IGPMStatusMessage.OperationCode
title: IGPMStatusMessage::OperationCode (gpmgmt.h)
description: Returns a code related to the GPMC operation.
helpviewer_keywords: ["GPMStatusMessage class [GPMC]","OperationCode method","IGPMStatusMessage interface [GPMC]","OperationCode method","IGPMStatusMessage.OperationCode","IGPMStatusMessage::OperationCode","OperationCode","OperationCode method [GPMC]","OperationCode method [GPMC]","GPMStatusMessage class","OperationCode method [GPMC]","IGPMStatusMessage interface","_win32_igpmstatusmessage_operationcode","gpmc.igpmstatusmessage_operationcode","gpmgmt/IGPMStatusMessage::OperationCode"]
old-location: gpmc\igpmstatusmessage_operationcode.htm
tech.root: gpmc
ms.assetid: f99dc90a-fabe-40fb-8289-36501a68b11d
ms.date: 12/05/2018
ms.keywords: GPMStatusMessage class [GPMC],OperationCode method, IGPMStatusMessage interface [GPMC],OperationCode method, IGPMStatusMessage.OperationCode, IGPMStatusMessage::OperationCode, OperationCode, OperationCode method [GPMC], OperationCode method [GPMC],GPMStatusMessage class, OperationCode method [GPMC],IGPMStatusMessage interface, _win32_igpmstatusmessage_operationcode, gpmc.igpmstatusmessage_operationcode, gpmgmt/IGPMStatusMessage::OperationCode
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
 - IGPMStatusMessage::OperationCode
 - gpmgmt/IGPMStatusMessage::OperationCode
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
 - IGPMStatusMessage.OperationCode
 - GPMStatusMessage.OperationCode
---

# IGPMStatusMessage::OperationCode


## -description

Returns a code related to the GPMC operation. The code corresponds to warnings or other errors that occurred during the operation. In the case of warnings, the operation continues. In the case of other errors, the operation stops.

The operation codes are internal identifiers that are defined in Gpmgmt.dll. You can extract a text description of the operation code by using the  <a href="/previous-versions/windows/desktop/gpmc/igpmstatusmessage-property-methods">Message property</a> of <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmessage">IGPMStatusMessage</a> or by using <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>.



## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmessage">IGPMStatusMessage</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>
