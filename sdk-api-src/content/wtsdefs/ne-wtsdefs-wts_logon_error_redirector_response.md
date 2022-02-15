---
UID: NE:wtsdefs._WTS_LOGON_ERROR_REDIRECTOR_RESPONSE
title: WTS_LOGON_ERROR_REDIRECTOR_RESPONSE (wtsdefs.h)
description: Contains values that specify the preferred response of the protocol to a logon error.
helpviewer_keywords: ["WRDS_LOGON_ERROR_REDIRECTOR_RESPONSE","WRDS_LOGON_ERROR_REDIRECTOR_RESPONSE enumeration [Remote Desktop Services]","WTS_LOGON_ERROR_REDIRECTOR_RESPONSE","WTS_LOGON_ERROR_REDIRECTOR_RESPONSE enumeration [Remote Desktop Services]","WTS_LOGON_ERR_HANDLED_DONT_SHOW","WTS_LOGON_ERR_HANDLED_DONT_SHOW_START_OVER","WTS_LOGON_ERR_HANDLED_SHOW","WTS_LOGON_ERR_INVALID","WTS_LOGON_ERR_NOT_HANDLED","termserv.wts_logon_error_redirector_response","wtsdefs/WRDS_LOGON_ERROR_REDIRECTOR_RESPONSE","wtsdefs/WTS_LOGON_ERROR_REDIRECTOR_RESPONSE","wtsdefs/WTS_LOGON_ERR_HANDLED_DONT_SHOW","wtsdefs/WTS_LOGON_ERR_HANDLED_DONT_SHOW_START_OVER","wtsdefs/WTS_LOGON_ERR_HANDLED_SHOW","wtsdefs/WTS_LOGON_ERR_INVALID","wtsdefs/WTS_LOGON_ERR_NOT_HANDLED"]
old-location: termserv\wts_logon_error_redirector_response.htm
tech.root: TermServ
ms.assetid: 67ed8d6f-641c-4739-911c-e61379e14048
ms.date: 12/05/2018
ms.keywords: WRDS_LOGON_ERROR_REDIRECTOR_RESPONSE, WRDS_LOGON_ERROR_REDIRECTOR_RESPONSE enumeration [Remote Desktop Services], WTS_LOGON_ERROR_REDIRECTOR_RESPONSE, WTS_LOGON_ERROR_REDIRECTOR_RESPONSE enumeration [Remote Desktop Services], WTS_LOGON_ERR_HANDLED_DONT_SHOW, WTS_LOGON_ERR_HANDLED_DONT_SHOW_START_OVER, WTS_LOGON_ERR_HANDLED_SHOW, WTS_LOGON_ERR_INVALID, WTS_LOGON_ERR_NOT_HANDLED, termserv.wts_logon_error_redirector_response, wtsdefs/WRDS_LOGON_ERROR_REDIRECTOR_RESPONSE, wtsdefs/WTS_LOGON_ERROR_REDIRECTOR_RESPONSE, wtsdefs/WTS_LOGON_ERR_HANDLED_DONT_SHOW, wtsdefs/WTS_LOGON_ERR_HANDLED_DONT_SHOW_START_OVER, wtsdefs/WTS_LOGON_ERR_HANDLED_SHOW, wtsdefs/WTS_LOGON_ERR_INVALID, wtsdefs/WTS_LOGON_ERR_NOT_HANDLED
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
req.typenames: WTS_LOGON_ERROR_REDIRECTOR_RESPONSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_LOGON_ERROR_REDIRECTOR_RESPONSE
 - wtsdefs/_WTS_LOGON_ERROR_REDIRECTOR_RESPONSE
 - WTS_LOGON_ERROR_REDIRECTOR_RESPONSE
 - wtsdefs/WTS_LOGON_ERROR_REDIRECTOR_RESPONSE
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
 - WTS_LOGON_ERROR_REDIRECTOR_RESPONSE
---

# WTS_LOGON_ERROR_REDIRECTOR_RESPONSE enumeration


## -description

Contains values that specify the preferred response of the protocol to a logon error.

## -enum-fields

### -field WTS_LOGON_ERR_INVALID:0

This value is used for safe initialization.

### -field WTS_LOGON_ERR_NOT_HANDLED

Specifies that the client logon was not handled by the redirector and should be handled by the logon user interface.

### -field WTS_LOGON_ERR_HANDLED_SHOW

Specifies that the client logon was handled by the redirector and that the logon user interface should display itself normally.

### -field WTS_LOGON_ERR_HANDLED_DONT_SHOW

Specifies that the client logon was handled by the redirector and should not be passed to the next redirector. The logon user interface should not display an error message but should attempt to collect credentials again.

### -field WTS_LOGON_ERR_HANDLED_DONT_SHOW_START_OVER

Specifies that the client logon was handled by the redirector and should not be passed to the next redirector.  The logon user interface should not be displayed and should not attempt to collect credentials again.

## -remarks

This enumeration is used by the following methods:

<ul>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocollogonerrorredirector-redirectstatus">RedirectStatus</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocollogonerrorredirector-redirectmessage">RedirectMessage</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocollogonerrorredirector-redirectlogonerror">RedirectLogonError</a>
</li>
</ul>
