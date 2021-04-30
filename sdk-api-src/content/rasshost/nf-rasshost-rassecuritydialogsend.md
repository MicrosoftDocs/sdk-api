---
UID: NF:rasshost.RasSecurityDialogSend
title: RasSecurityDialogSend function (rasshost.h)
description: The RasSecurityDialogSend function sends a message to be displayed in a terminal window on a remote computer. A third-party RAS security DLL sends this message as part of its authentication of a remote user.
helpviewer_keywords: ["RasSecurityDialogSend","RasSecurityDialogSend function [RAS]","_ras_rassecuritydialogsend","rasshost/RasSecurityDialogSend","rras.rassecuritydialogsend"]
old-location: rras\rassecuritydialogsend.htm
tech.root: RRAS
ms.assetid: adbc357b-7a5d-426d-b21f-0b1478bb2348
ms.date: 12/05/2018
ms.keywords: RasSecurityDialogSend, RasSecurityDialogSend function [RAS], _ras_rassecuritydialogsend, rasshost/RasSecurityDialogSend, rras.rassecuritydialogsend
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
 - RasSecurityDialogSend
 - rasshost/RasSecurityDialogSend
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
 - RasSecurityDialogSend
---

# RasSecurityDialogSend function


## -description

The 
<b>RasSecurityDialogSend</b> function sends a message to be displayed in a terminal window on a remote computer. A third-party RAS security DLL sends this message as part of its authentication of a remote user.

To call this function, first call the 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function to load Rasman.dll. Then call the 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function to get the DLL's 
<b>RasSecurityDialogSend</b> entry point.
<div class="alert"><b>Note</b>  Windows Server 2008, 
  Windows Server 2003,
  Windows 2000 Server, and
  Windows NT Server 4.0 currently provide RAS security host support for serial devices only. Other types of connections, such as Integrated Services Digital Network (ISDN) or virtual private network (VPN) connections, are not supported.</div><div> </div>

## -parameters

### -param hPort [in]

Specifies the port handle that the RAS server passed to the security DLL in the 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogbegin">RasSecurityDialogBegin</a> call for this authentication transaction.

### -param pBuffer [in]

Pointer to the send buffer that was passed to the security DLL in the call to 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogbegin">RasSecurityDialogBegin</a>. Before calling 
<b>RasSecurityDialogSend</b>, copy into this buffer the message to send to the remote user. The <i>SendBufSize</i> parameter of the 
<b>RasSecurityDialogBegin</b> function indicates the maximum number of bytes the buffer can store.

### -param BufferLength [in]

Specifies the number of bytes to send in the <i>pBuffer</i> buffer.

## -returns

If the function is successful, the return value is PENDING (defined in Raserror.h). This indicates that the send operation is in progress.

If an error occurs, the return value is one of the error codes defined in Raserror.h or Winerror.h. 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> does not provide extended error information.

## -remarks

The 
<b>RasSecurityDialogSend</b> function is asynchronous. After calling it to send a message to the remote user, call the 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogreceive">RasSecurityDialogReceive</a> function, and then wait for a response. The security DLL can make any number of 
<b>RasSecurityDialogSend</b> calls, with each call followed by a 
<b>RasSecurityDialogReceive</b> call.

When a security DLL is authenticating a remote user, the connection operation on the remote computer enters a RASCS_Interactive paused state. The message sent by 
<b>RasSecurityDialogSend</b> is displayed as output in a terminal window on the remote computer. The response received by 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogreceive">RasSecurityDialogReceive</a> is the input that the remote user types in the terminal window. The RASCS_Interactive value is defined in the 
<a href="/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCONNSTATE</a> enumeration.

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/RRAS/ras-server-administration-functions">RAS Server Administration Functions</a>



<a href="/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCONNSTATE</a>



<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogbegin">RasSecurityDialogBegin</a>



<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogreceive">RasSecurityDialogReceive</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>