---
UID: NF:rasshost.RasSecurityDialogGetInfo
title: RasSecurityDialogGetInfo function (rasshost.h)
description: The RasSecurityDialogGetInfo function is called by a RAS security DLL to get information about a port from the RAS server.
helpviewer_keywords: ["RasSecurityDialogGetInfo","RasSecurityDialogGetInfo function [RAS]","_ras_rassecuritydialoggetinfo","rasshost/RasSecurityDialogGetInfo","rras.rassecuritydialoggetinfo"]
old-location: rras\rassecuritydialoggetinfo.htm
tech.root: RRAS
ms.assetid: b7fbcfb6-686c-4464-ba78-e689019e74be
ms.date: 12/05/2018
ms.keywords: RasSecurityDialogGetInfo, RasSecurityDialogGetInfo function [RAS], _ras_rassecuritydialoggetinfo, rasshost/RasSecurityDialogGetInfo, rras.rassecuritydialoggetinfo
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
 - RasSecurityDialogGetInfo
 - rasshost/RasSecurityDialogGetInfo
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
 - RasSecurityDialogGetInfo
---

# RasSecurityDialogGetInfo function


## -description

The 
<b>RasSecurityDialogGetInfo</b> function is called by a RAS security DLL to get information about a port from the RAS server.

To call this function, first call the 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function to load Rasman.dll. Then call the 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function to get the DLL's 
<b>RasSecurityDialogGetInfo</b> entry point.
<div class="alert"><b>Note</b>  Windows Server 2008, 
  Windows Server 2003,
  Windows 2000 Server, and
  Windows NT Server 4.0 currently provide RAS security host support for serial devices only. Other types of connections, such as Integrated Services Digital Network (ISDN) or virtual private network (VPN) connections, are not supported.</div><div> </div>

## -parameters

### -param hPort [in]

Specifies the port handle that the RAS server passed to the security DLL in the 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogbegin">RasSecurityDialogBegin</a> call for this authentication transaction.

### -param pBuffer [in]

Pointer to the 
<a href="/windows/desktop/api/rasshost/ns-rasshost-ras_security_info">RAS_SECURITY_INFO</a> structure that receives information about the specified RAS port.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the error codes defined in Raserror.h or Winerror.h. 
<a href="/previous-versions/windows/desktop/wab/-wab-iabcontainer-getlasterror">GetLastError</a> does not provide extended error information.

## -remarks

The 
<b>RasSecurityDialogGetInfo</b> function retrieves information about the port associated with a RAS security DLL authentication transaction.

The <b>LastError</b> member of the 
<a href="/windows/desktop/api/rasshost/ns-rasshost-ras_security_info">RAS_SECURITY_INFO</a> structure indicates the state of the last 
<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogreceive">RasSecurityDialogReceive</a> call for the port. If the receive operation has been completed successfully, <b>LastError</b> is SUCCESS and the <b>BytesReceived</b> member indicates the number of bytes received. Otherwise, <b>LastError</b> is PENDING if the receive operation is still in progress, or a nonzero error code if the receive operation failed.

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/RRAS/ras-server-administration-functions">RAS Server Administration Functions</a>



<a href="/windows/desktop/api/rasshost/ns-rasshost-ras_security_info">RAS_SECURITY_INFO</a>



<a href="/windows/desktop/api/rasshost/nf-rasshost-rassecuritydialogreceive">RasSecurityDialogReceive</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>