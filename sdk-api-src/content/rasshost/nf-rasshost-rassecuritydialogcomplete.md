---
UID: NF:rasshost.RasSecurityDialogComplete
title: RasSecurityDialogComplete function (rasshost.h)
description: The RasSecurityDialogComplete function notifies the RAS server of the results of a third-party security authentication transaction.
helpviewer_keywords: ["RasSecurityDialogComplete","RasSecurityDialogComplete function [RAS]","_ras_rassecuritydialogcomplete","rasshost/RasSecurityDialogComplete","rras.rassecuritydialogcomplete"]
old-location: rras\rassecuritydialogcomplete.htm
tech.root: RRAS
ms.assetid: 9ebe8b85-7500-405f-98c2-6f51f3339629
ms.date: 12/05/2018
ms.keywords: RasSecurityDialogComplete, RasSecurityDialogComplete function [RAS], _ras_rassecuritydialogcomplete, rasshost/RasSecurityDialogComplete, rras.rassecuritydialogcomplete
req.header: rasshost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Rasman.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasSecurityDialogComplete
 - rasshost/RasSecurityDialogComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasman.dll
api_name:
 - RasSecurityDialogComplete
---

# RasSecurityDialogComplete function


## -description

The 
<b>RasSecurityDialogComplete</b> function notifies the RAS server of the results of a third-party security authentication transaction. A third-party RAS security DLL calls 
<b>RasSecurityDialogComplete</b> when it has completed its authentication of the remote user.

The RAS server passes a pointer to the 
<b>RasSecurityDialogComplete</b> function when the server calls the 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogbegin">RasSecurityDialogBegin</a> entry point of the security DLL.
<div class="alert"><b>Note</b>  Windows Server 2008, 
  Windows Server 2003,
  Windows 2000 Server, and
  Windows NT Server 4.0 currently provide RAS security host support for serial devices only. Other types of connections, such as Integrated Services Digital Network (ISDN) or virtual private network (VPN) connections, are not supported.</div><div> </div>

## -parameters

### -param pSecMsg [in]

Pointer to the 
<a href="/windows/desktop/api/rasshost/ns-rasshost-security_message">SECURITY_MESSAGE</a> structure that specifies the results of the authentication transaction.

## -remarks

When a security DLL has finished authenticating the remote user, it calls the 
<b>RasSecurityDialogComplete</b> function to report the results. The RAS server then performs a cleanup sequence. As part of this cleanup sequence, the RAS server calls the security DLL's 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogend">RasSecurityDialogEnd</a> function to give the DLL an opportunity to perform its own cleanup, if necessary.

## -see-also

<a href="/windows/desktop/RRAS/ras-server-administration-functions">RAS Server Administration Functions</a>



<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogbegin">RasSecurityDialogBegin</a>



<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogend">RasSecurityDialogEnd</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/api/rasshost/ns-rasshost-security_message">SECURITY_MESSAGE</a>