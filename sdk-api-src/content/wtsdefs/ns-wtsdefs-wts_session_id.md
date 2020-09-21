---
UID: NS:wtsdefs._WTS_SESSION_ID
title: WTS_SESSION_ID (wtsdefs.h)
description: Contains a GUID that uniquely identifies a session.
helpviewer_keywords: ["*PWTS_SESSION_ID","PWRDS_SESSION_ID","PWRDS_SESSION_ID structure pointer [Remote Desktop Services]","PWTS_SESSION_ID","PWTS_SESSION_ID structure pointer [Remote Desktop Services]","WRDS_SESSION_ID","WRDS_SESSION_ID structure [Remote Desktop Services]","WTS_SESSION_ID","WTS_SESSION_ID structure [Remote Desktop Services]","termserv.wts_session_id","wtsdefs/PWRDS_SESSION_ID","wtsdefs/PWTS_SESSION_ID","wtsdefs/WRDS_SESSION_ID","wtsdefs/WTS_SESSION_ID"]
old-location: termserv\wts_session_id.htm
tech.root: TermServ
ms.assetid: fe0714ec-c670-40b7-9808-2171abae79a8
ms.date: 12/05/2018
ms.keywords: '*PWTS_SESSION_ID, PWRDS_SESSION_ID, PWRDS_SESSION_ID structure pointer [Remote Desktop Services], PWTS_SESSION_ID, PWTS_SESSION_ID structure pointer [Remote Desktop Services], WRDS_SESSION_ID, WRDS_SESSION_ID structure [Remote Desktop Services], WTS_SESSION_ID, WTS_SESSION_ID structure [Remote Desktop Services], termserv.wts_session_id, wtsdefs/PWRDS_SESSION_ID, wtsdefs/PWTS_SESSION_ID, wtsdefs/WRDS_SESSION_ID, wtsdefs/WTS_SESSION_ID'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WTS_SESSION_ID, *PWTS_SESSION_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_SESSION_ID
 - wtsdefs/_WTS_SESSION_ID
 - PWTS_SESSION_ID
 - wtsdefs/PWTS_SESSION_ID
 - WTS_SESSION_ID
 - wtsdefs/WTS_SESSION_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WTS_SESSION_ID
---

# WTS_SESSION_ID structure


## -description

Contains a <b>GUID</b> that uniquely identifies a session.

## -struct-fields

### -field SessionUniqueGuid

A GUID that specifies the client connection.

### -field SessionId

An integer that specifies the session associated with the client connection.

## -remarks

This structure is used in the following methods:

<ul>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-authenticateclienttosession">AuthenticateClientToSession</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify">LogonNotify</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid">NotifySessionId</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-authenticateclienttosession">AuthenticateClientToSession</a>



<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify">LogonNotify</a>



<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid">NotifySessionId</a>



<a href="/windows/desktop/TermServ/custom-remote-protocol-structures">Remote Desktop Protocol Provider Structures</a>