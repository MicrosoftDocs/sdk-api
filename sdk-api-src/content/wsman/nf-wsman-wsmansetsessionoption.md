---
UID: NF:wsman.WSManSetSessionOption
title: WSManSetSessionOption function (wsman.h)
description: Sets an extended set of options for the session.
helpviewer_keywords: ["WSManSetSessionOption","WSManSetSessionOption function [Windows Remote Management]","winrm.wsmansetsessionoption","wsman/WSManSetSessionOption"]
old-location: winrm\wsmansetsessionoption.htm
tech.root: winrm
ms.assetid: e6d21412-49c5-4e04-974d-28e0165ddb69
ms.date: 12/05/2018
ms.keywords: WSManSetSessionOption, WSManSetSessionOption function [Windows Remote Management], winrm.wsmansetsessionoption, wsman/WSManSetSessionOption
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
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
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManSetSessionOption
 - wsman/WSManSetSessionOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManSetSessionOption
---

# WSManSetSessionOption function


## -description

Sets an extended set of options for the session.

## -parameters

### -param session [in]

Specifies the session handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreatesession">WSManCreateSession</a> call.  This parameter cannot be <b>NULL</b>.

### -param option

Specifies the option to be set. This parameter must be set to one of the values in the <a href="/windows/desktop/api/wsman/ne-wsman-wsmansessionoption">WSManSessionOption</a> enumeration.

### -param data [in]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure that defines the option value.

## -returns

This method returns zero on success. Otherwise, this method returns an error code.

## -remarks

If the <b>WSManSetSessionOption</b> method is called with different values specified for the <i>option</i> parameter, the order of the different options is important. The first  time <b>WSManSetSessionOption</b> is called, the transport is set for the session. If a second call requests a different type of transport, the call will fail.

For example, the second method call will fail if the methods are called in the following order:

<ul>
<li><code>WSManSetSessionOption(WSMAN_OPTION_UNENCRYPTED_MESSAGES)</code></li>
<li><code>WSManSetSessionOption(WSMAN_OPTION_ALLOW_NEGOTIATE_IMPLICIT_CREDENTIALS)</code></li>
</ul>
The first method call sets the transport to HTTP because the <i>option</i> parameter is set to <b>WSMAN_OPTION_UNENCRYPTED_MESSAGES</b>.  The second call fails because the option that was passed is applicable for HTTPS and the transport was set to HTTP by the first message.