---
UID: NS:npapi._NOTIFYINFO
title: NOTIFYINFO (npapi.h)
description: The NOTIFYINFO structure contains status information about a network connect or disconnect operation. It is used by the AddConnectNotify and CancelConnectNotify functions.
helpviewer_keywords: ["*LPNOTIFYINFO","LPNOTIFYINFO","LPNOTIFYINFO structure pointer [Security]","NOTIFYINFO","NOTIFYINFO structure [Security]","_mnp_notifyinfo","npapi/LPNOTIFYINFO","npapi/NOTIFYINFO","security.notifyinfo"]
old-location: security\notifyinfo.htm
tech.root: security
ms.assetid: 43b31128-da9c-470b-b030-0010b250a291
ms.date: 12/05/2018
ms.keywords: '*LPNOTIFYINFO, LPNOTIFYINFO, LPNOTIFYINFO structure pointer [Security], NOTIFYINFO, NOTIFYINFO structure [Security], _mnp_notifyinfo, npapi/LPNOTIFYINFO, npapi/NOTIFYINFO, security.notifyinfo'
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
req.typenames: NOTIFYINFO, *LPNOTIFYINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NOTIFYINFO
 - npapi/_NOTIFYINFO
 - LPNOTIFYINFO
 - npapi/LPNOTIFYINFO
 - NOTIFYINFO
 - npapi/NOTIFYINFO
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
 - NOTIFYINFO
---

# NOTIFYINFO structure


## -description

The <b>NOTIFYINFO</b> structure contains status information about a network connect or disconnect operation. It is used by the 
<a href="/windows/desktop/api/npapi/nf-npapi-addconnectnotify">AddConnectNotify</a> and 
<a href="/windows/desktop/api/npapi/nf-npapi-cancelconnectnotify">CancelConnectNotify</a> functions.

## -struct-fields

### -field dwNotifyStatus

This will be either NOTIFY_PRE or NOTIFY_POST to indicate whether this notification is sent before or after the connection or disconnection is performed.

### -field dwOperationStatus

This is set to WN_SUCCESS when <b>dwNotifyStatus</b> is NOTIFY_PRE. 




If <b>dwNotifyStatus</b> is set to NOTIFY_POST, <b>dwOperationStatus</b> contains the return status code from the function performing the operation: 
<a href="/windows/desktop/api/npapi/nf-npapi-npaddconnection">NPAddConnection</a> or 
<a href="/windows/desktop/api/npapi/nf-npapi-npcancelconnection">NPCancelConnection</a>.

### -field lpContext

Used by the application receiving the notification in order to keep a context for the operation between the pre-notification and the post-notification calls. In other words, it enables the notification application to match the advance notification call to the corresponding after-the-fact notification call for a particular event. The <b>lpContext</b> member is a <b>NULL</b> pointer when the notification function is called for advance notification. The notification function can return with <b>lpContext</b> still <b>NULL</b>, indicating that it is not interested in further notification for this specific operation. In this case, the notification function will not be called again with after-the-fact notification for this operation. If the advance notification function call returns a non-<b>NULL</b> value in <b>lpContext</b>, this value is passed in when the notification function is called for the after-the-fact notification for that same operation.