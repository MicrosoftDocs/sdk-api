---
UID: NF:iscsidsc.LogoutIScsiTarget
title: LogoutIScsiTarget function (iscsidsc.h)
description: The LogoutIscsiTarget routine closes the specified login session.
helpviewer_keywords: ["LogoutIScsiTarget","LogoutIscsiTarget","LogoutIscsiTarget function [iSCSI Discovery Library API]","iscsidisc.logoutiscsitarget","iscsidsc/LogoutIscsiTarget"]
old-location: iscsidisc\logoutiscsitarget.htm
tech.root: iSCSIDisc
ms.assetid: c49ad2e2-3f06-48e7-bf38-6074f9a6bcad
ms.date: 12/05/2018
ms.keywords: LogoutIScsiTarget, LogoutIscsiTarget, LogoutIscsiTarget function [iSCSI Discovery Library API], iscsidisc.logoutiscsitarget, iscsidsc/LogoutIscsiTarget
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LogoutIScsiTarget
 - iscsidsc/LogoutIScsiTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - LogoutIscsiTarget
---

# LogoutIScsiTarget function


## -description

The <b>LogoutIscsiTarget</b> routine closes the specified login session.

## -parameters

### -param UniqueSessionId [in]

A pointer to a structure of type <a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a> that contains a unique session identifier for the login session end.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -remarks

If the login session is not for informational purposes, the iSCSI initiator service ensures that all devices associated with the session can be safely removed from the device stack before allowing the initiator to close the session. If the session is an informational session, the iSCSI initiator service closes the session immediately.

## -see-also

<a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-loginiscsitargeta">LoginIscsiTarget</a>