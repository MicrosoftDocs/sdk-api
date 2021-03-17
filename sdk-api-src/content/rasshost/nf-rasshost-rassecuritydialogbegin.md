---
UID: NF:rasshost.RasSecurityDialogBegin
title: RasSecurityDialogBegin function (rasshost.h)
description: The RasSecurityDialogBegin function is a third-party RAS security DLL entry point that the RAS server calls when a remote user tries to connect. This enables the security DLL to begin its authentication of the remote user.
helpviewer_keywords: ["RasSecurityDialogBegin","RasSecurityDialogBegin callback","RasSecurityDialogBegin callback function [RAS]","_ras_rassecuritydialogbegin","rasshost/RasSecurityDialogBegin","rras.rassecuritydialogbegin"]
old-location: rras\rassecuritydialogbegin.htm
tech.root: RRAS
ms.assetid: 19f4591b-ecae-478b-b110-c0d88c72f7eb
ms.date: 12/05/2018
ms.keywords: RasSecurityDialogBegin, RasSecurityDialogBegin callback, RasSecurityDialogBegin callback function [RAS], _ras_rassecuritydialogbegin, rasshost/RasSecurityDialogBegin, rras.rassecuritydialogbegin
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
 - RasSecurityDialogBegin
 - rasshost/RasSecurityDialogBegin
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
 - RasSecurityDialogBegin
---

# RasSecurityDialogBegin function


## -description

The 
<b>RasSecurityDialogBegin</b> function is a third-party RAS security DLL entry point that the RAS server calls when a remote user tries to connect. This enables the security DLL to begin its authentication of the remote user.
<div class="alert"><b>Note</b>  Windows Server 2008, 
  Windows Server 2003,
  Windows 2000 Server, and
  Windows NT Server 4.0 currently provide RAS security host support for serial devices only. Other types of connections, such as Integrated Services Digital Network (ISDN) or virtual private network (VPN) connections, are not supported.</div><div> </div>

## -parameters

### -param hPort [in]

Specifies a RAS port handle. The security DLL uses this handle in other RAS security functions, such as 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogsend">RasSecurityDialogSend</a> and 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogreceive">RasSecurityDialogReceive</a>, to identify this authentication transaction. 




Note that this handle is valid only in RAS security functions; do not use it in other I/O functions.

### -param pSendBuf [in]

Pointer to a buffer allocated by the RAS server. The security DLL uses this buffer with the 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogsend">RasSecurityDialogSend</a> function to send text that is displayed in the RAS terminal window on the remote computer.

### -param SendBufSize [in]

Specifies the size, in bytes, of the <i>pSendBuf</i> buffer.

### -param pRecvBuf [in]

Pointer to a buffer allocated by the RAS server. The security DLL uses this buffer with the 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogreceive">RasSecurityDialogReceive</a> function to receive the response from the remote user.

### -param RecvBufSize [in]

Specifies the size, in bytes, of the <i>pRecvBuf</i> buffer.

### -param VOID [in]

Pointer to the 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogcomplete">RasSecurityDialogComplete</a> function. When the security DLL has completed the authentication of the remote user, it calls this function to report the results to the RAS server.

This callback function has no parameters.

## -returns

If the security DLL successfully starts the authentication operation, 
<b>RasSecurityDialogBegin</b> should return <b>NO_ERROR</b>. In this case, the security DLL must later terminate the authentication transaction by calling the function pointed to by the <i>RasSecurityDialogComplete</i> parameter.

If an error occurs, 
<b>RasSecurityDialogBegin</b> should return a nonzero error code. In this case, the RAS server hangs up the call and records the error in the event log. Returning a nonzero error code terminates the authentication transaction, so the security DLL does not need to call the <a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogcomplete">RasSecurityDialogComplete</a> function.

## -remarks

When a  RAS server receives a call from a remote computer, it calls the 
<b>RasSecurityDialogBegin</b> function exported by the registered RAS security DLL, if there is one. When the RAS server calls this function, it passes the following information to the security DLL:

<ul>
<li>A port handle to identify the connection</li>
<li>Pointers to buffers to use when communicating with the remote user</li>
<li>A pointer to the 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogcomplete">RasSecurityDialogComplete</a> function to call when the authentication has been completed</li>
</ul>
The port handle and buffer pointers are valid until 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogcomplete">RasSecurityDialogComplete</a> is called to terminate the authentication transaction.

The 
<b>RasSecurityDialogBegin</b> implementation must return as soon as possible, because the RAS server is blocked and cannot accept any other calls until 
<b>RasSecurityDialogBegin</b> returns. The 
<b>RasSecurityDialogBegin</b> function should copy the input parameters and create a thread to communicate with and authenticate the remote user.

## -see-also

<a href="/windows/desktop/RRAS/ras-server-administration-functions">RAS Server Administration Functions</a>



<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogcomplete">RasSecurityDialogComplete</a>



<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogreceive">RasSecurityDialogReceive</a>



<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogsend">RasSecurityDialogSend</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>