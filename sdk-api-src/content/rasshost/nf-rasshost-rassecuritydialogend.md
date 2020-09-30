---
UID: NF:rasshost.RasSecurityDialogEnd
title: RasSecurityDialogEnd function (rasshost.h)
description: The RasSecurityDialogEnd function is a third-party RAS security DLL entry point that the RAS server calls to terminate an authentication transaction.
helpviewer_keywords: ["RasSecurityDialogEnd","RasSecurityDialogEnd callback","RasSecurityDialogEnd callback function [RAS]","_ras_rassecuritydialogend","rasshost/RasSecurityDialogEnd","rras.rassecuritydialogend"]
old-location: rras\rassecuritydialogend.htm
tech.root: RRAS
ms.assetid: 52274d37-baed-4ab9-8019-123ae7c5b0fc
ms.date: 12/05/2018
ms.keywords: RasSecurityDialogEnd, RasSecurityDialogEnd callback, RasSecurityDialogEnd callback function [RAS], _ras_rassecuritydialogend, rasshost/RasSecurityDialogEnd, rras.rassecuritydialogend
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasSecurityDialogEnd
 - rasshost/RasSecurityDialogEnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Rasshost.h
api_name:
 - RasSecurityDialogEnd
---

# RasSecurityDialogEnd function


## -description

The 
<b>RasSecurityDialogEnd</b> function is a third-party RAS security DLL entry point that the RAS server calls to terminate an authentication transaction.
<div class="alert"><b>Note</b>  Windows Server 2008, 
  Windows Server 2003,
  Windows 2000 Server, and
  Windows NT Server 4.0 currently provide RAS security host support for serial devices only. Other types of connections, such as Integrated Services Digital Network (ISDN) or virtual private network (VPN) connections, are not supported.</div><div> </div>

## -parameters

### -param hPort [in]

Specifies the port handle that the RAS server passed to the security DLL in the 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogbegin">RasSecurityDialogBegin</a> call for this authentication transaction.

## -returns

If the security DLL returns <b>NO_ERROR</b>, the RAS server does not terminate the authentication transaction. In this case, the security DLL must later call the 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogcomplete">RasSecurityDialogComplete</a> function when it is ready to terminate.

If the security DLL returns a nonzero error code, the RAS server terminates the authentication transaction. In this case, the security DLL does not need to make another 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogcomplete">RasSecurityDialogComplete</a> call. Return an error code defined in Winerror.h or Raserror.h, such as <b>ERROR_PORT_DISCONNECTED</b>.

## -remarks

When a security DLL has finished authenticating the remote user, it calls the 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogcomplete">RasSecurityDialogComplete</a> function. The RAS server then performs a cleanup sequence that includes a call to the DLL's 
<b>RasSecurityDialogEnd</b> function. This gives the security DLL an opportunity to perform any necessary cleanup. To terminate the authentication transaction, 
<b>RasSecurityDialogEnd</b> must return a nonzero error code.

The RAS server may also call 
<b>RasSecurityDialogEnd</b> if it needs to abnormally terminate the authentication transaction before the security DLL calls 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogcomplete">RasSecurityDialogComplete</a>. In this case, the security DLL should terminate the worker thread associated with the <i>hPort</i> port handle, and perform any other necessary cleanup. If 
<b>RasSecurityDialogEnd</b> returns a nonzero value, the security DLL does not need to call 
<b>RasSecurityDialogComplete</b>.

For both normal and abnormal termination, the 
<b>RasSecurityDialogEnd</b> function returns NO_ERROR to delay the termination. If it does so, it must later call 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogcomplete">RasSecurityDialogComplete</a> when it is ready to terminate.

## -see-also

<a href="/windows/desktop/RRAS/ras-server-administration-functions">RAS Server Administration Functions</a>



<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogbegin">RasSecurityDialogBegin</a>



<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogcomplete">RasSecurityDialogComplete</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>