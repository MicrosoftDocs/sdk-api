---
UID: NS:npapi._NOTIFYCANCEL
title: NOTIFYCANCEL (npapi.h)
description: The NOTIFYCANCEL structure contains the details of a network disconnect operation. It is used by the CancelConnectNotify function.
helpviewer_keywords: ["*LPNOTIFYCANCEL","LPNOTIFYCANCEL","LPNOTIFYCANCEL structure pointer [Security]","NOTIFYCANCEL","NOTIFYCANCEL structure [Security]","_mnp_notifycancel","npapi/LPNOTIFYCANCEL","npapi/NOTIFYCANCEL","security.notifycancel"]
old-location: security\notifycancel.htm
tech.root: security
ms.assetid: cc4cb0fb-ff7d-4bdc-944c-3bf9b08ea72c
ms.date: 12/05/2018
ms.keywords: '*LPNOTIFYCANCEL, LPNOTIFYCANCEL, LPNOTIFYCANCEL structure pointer [Security], NOTIFYCANCEL, NOTIFYCANCEL structure [Security], _mnp_notifycancel, npapi/LPNOTIFYCANCEL, npapi/NOTIFYCANCEL, security.notifycancel'
req.header: npapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NOTIFYCANCEL, *LPNOTIFYCANCEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NOTIFYCANCEL
 - npapi/_NOTIFYCANCEL
 - LPNOTIFYCANCEL
 - npapi/LPNOTIFYCANCEL
 - NOTIFYCANCEL
 - npapi/NOTIFYCANCEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Npapi.h
api_name:
 - NOTIFYCANCEL
---

# NOTIFYCANCEL structure


## -description

The <b>NOTIFYCANCEL</b> structure contains the details of a network disconnect operation. It is used by the 
<a href="/windows/desktop/api/npapi/nf-npapi-cancelconnectnotify">CancelConnectNotify</a> function.

## -struct-fields

### -field lpName

Pointer to the name of the local device or network resource whose connection is being canceled.

### -field lpProvider

For advance notification, this field is not defined. The MPR will try all valid providers to cancel the connection. 




For after-the-fact notification, if the cancel operation was successful, this field specifies the name of the network provider that canceled the connection.

### -field dwFlags

Currently, the only flag supported is CONNECT_UPDATE_PROFILE, which indicates whether the disconnection should remain persistent. If this flag is set, Windows no longer restores this connection when the user logs on.

### -field fForce

Indicates whether the disconnect should continue even if there are open files or jobs on the connection. If this field is <b>TRUE</b>, the connection is canceled regardless of open files or jobs. If this field is <b>FALSE</b>, the connection will not be canceled if there are open files or jobs.