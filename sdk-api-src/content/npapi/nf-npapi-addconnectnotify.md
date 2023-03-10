---
UID: NF:npapi.AddConnectNotify
title: AddConnectNotify function (npapi.h)
description: Called before and after each add connection operation (WNetAddConnection, WNetAddConnection2, and WNetAddConnection3) is attempted by the Multiple Provider Router (MPR).
helpviewer_keywords: ["AddConnectNotify","AddConnectNotify function [Security]","_mnp_addconnectnotify","npapi/AddConnectNotify","security.addconnectnotify"]
old-location: security\addconnectnotify.htm
tech.root: security
ms.assetid: a061b088-81ca-4276-a0d6-9f1d1282a039
ms.date: 12/05/2018
ms.keywords: AddConnectNotify, AddConnectNotify function [Security], _mnp_addconnectnotify, npapi/AddConnectNotify, security.addconnectnotify
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
 - AddConnectNotify
 - npapi/AddConnectNotify
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
 - AddConnectNotify
---

# AddConnectNotify function


## -description

The <b>AddConnectNotify</b> function is called before and after each add connection operation (<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona">WNetAddConnection</a>, 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnection2</a>, and 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a">WNetAddConnection3</a>) is attempted by the <a href="/windows/desktop/SecGloss/m-gly">Multiple Provider Router</a> (MPR).

The <b>AddConnectNotify</b> function is not called when MPR is automatically restoring network connections.

## -parameters

### -param lpNotifyInfo [in, out]

A pointer to a 
<a href="/windows/desktop/api/npapi/ns-npapi-notifyinfo">NOTIFYINFO</a> structure that contains information about the notification.

### -param lpAddInfo [in]

A pointer to a 
<a href="/windows/desktop/api/npapi/ns-npapi-notifyadd">NOTIFYADD</a> structure that contains information about the connection being added.

## -returns

If the function succeeds, the function should return WN_SUCCESS.

If the function fails, it should return an error code. This can be any of the error codes specified in 
<a href="/windows/desktop/SecAuthN/network-security-return-values">Network Security Return Values</a>.

## -remarks

The <b>AddConnectNotify</b> function is implemented by applications that need to receive notification from the MPR when a network resource is connected or disconnected. For more information about how to write an application that receives such notifications, see 
<a href="/windows/desktop/SecAuthN/receiving-connection-notifications">Receiving Connection Notifications</a>.

## -see-also

<a href="/windows/desktop/api/npapi/nf-npapi-cancelconnectnotify">CancelConnectNotify</a>