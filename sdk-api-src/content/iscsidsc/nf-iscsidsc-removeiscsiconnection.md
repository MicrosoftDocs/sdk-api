---
UID: NF:iscsidsc.RemoveIScsiConnection
title: RemoveIScsiConnection function (iscsidsc.h)
description: RemoveIscsiConnection function removes a connection from an active session.
helpviewer_keywords: ["RemoveIScsiConnection","RemoveIscsiConnection","RemoveIscsiConnection function [iSCSI Discovery Library API]","iscsidisc.removeiscsiconnection","iscsidsc/RemoveIscsiConnection"]
old-location: iscsidisc\removeiscsiconnection.htm
tech.root: iSCSIDisc
ms.assetid: 1d34348a-b16a-4420-88e1-092e3f521ea5
ms.date: 12/05/2018
ms.keywords: RemoveIScsiConnection, RemoveIscsiConnection, RemoveIscsiConnection function [iSCSI Discovery Library API], iscsidisc.removeiscsiconnection, iscsidsc/RemoveIscsiConnection
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
 - RemoveIScsiConnection
 - iscsidsc/RemoveIScsiConnection
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
 - RemoveIscsiConnection
---

# RemoveIScsiConnection function


## -description

The <b>RemoveIscsiConnection</b> function removes a connection from an active session.

## -parameters

### -param UniqueSessionId [in]

A pointer to a structure of type <a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a> that specifies the unique session identifier of the session that the connection belongs to.

### -param ConnectionId [in]

A pointer to a structure of type <a href="/previous-versions/windows/desktop/legacy/bb870817(v=vs.85)">ISCSI_UNIQUE_CONNECTION_ID</a> that specifies the connection to remove.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -remarks

The <b>RemoveIscsiConnection</b> function will not remove the last connection of a session or the leading connection of a session. The caller must close the session by calling <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-logoutiscsitarget">LogoutIscsiTarget</a> to remove the last connection.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-logoutiscsitarget">LogoutIscsiTarget</a>