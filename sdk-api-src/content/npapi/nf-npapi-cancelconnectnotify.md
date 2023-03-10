---
UID: NF:npapi.CancelConnectNotify
title: CancelConnectNotify function (npapi.h)
description: Calls CancelConnectNotify before and after each cancel connection operation (WNetCancelConnection and WNetCancelConnection2).
helpviewer_keywords: ["CancelConnectNotify","CancelConnectNotify function [Security]","_mnp_cancelconnectnotify","npapi/CancelConnectNotify","security.cancelconnectnotify"]
old-location: security\cancelconnectnotify.htm
tech.root: security
ms.assetid: 94bd969d-f94d-449c-971d-d17fff2c07e1
ms.date: 12/05/2018
ms.keywords: CancelConnectNotify, CancelConnectNotify function [Security], _mnp_cancelconnectnotify, npapi/CancelConnectNotify, security.cancelconnectnotify
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CancelConnectNotify
 - npapi/CancelConnectNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - CancelConnectNotify
---

# CancelConnectNotify function


## -description

The <a href="/windows/desktop/SecGloss/m-gly">Multiple Provider Router</a> (MPR) calls <b>CancelConnectNotify</b> before and after each cancel connection operation (<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona">WNetCancelConnection</a> and 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a">WNetCancelConnection2</a>).

## -parameters

### -param lpNotifyInfo [in, out]

A pointer to a 
<a href="/windows/desktop/api/npapi/ns-npapi-notifyinfo">NOTIFYINFO</a> structure that contains information about the notification.

### -param lpCancelInfo [in]

A pointer to a 
<a href="/windows/desktop/api/npapi/ns-npapi-notifycancel">NOTIFYCANCEL</a> structure that contains the cancel connection specific information.

## -returns

If the function succeeds, the function should return WN_SUCCESS.

If the function fails, it should return an error code. This can be any of the error codes specified in 
<a href="/windows/desktop/SecAuthN/network-security-return-values">Network Security Return Values</a>.

## -remarks

The <b>CancelConnectNotify</b> function is implemented by applications that need to receive notification from the MPR when a network resource is connected or disconnected. For more information about how to write an application that receives such notifications, see 
<a href="/windows/desktop/SecAuthN/receiving-connection-notifications">Receiving Connection Notifications</a>.

## -see-also

<a href="/windows/desktop/api/npapi/nf-npapi-addconnectnotify">AddConnectNotify</a>