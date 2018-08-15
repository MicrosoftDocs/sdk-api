---
UID: NF:rasshost.RasSecurityDialogGetInfo
title: RasSecurityDialogGetInfo function
author: windows-sdk-content
description: The RasSecurityDialogGetInfo function is called by a RAS security DLL to get information about a port from the RAS server.
old-location: rras\rassecuritydialoggetinfo.htm
old-project: rras
ms.assetid: b7fbcfb6-686c-4464-ba78-e689019e74be
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RasSecurityDialogGetInfo, RasSecurityDialogGetInfo function [RAS], _ras_rassecuritydialoggetinfo, rasshost/RasSecurityDialogGetInfo, rras.rassecuritydialoggetinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rasshost.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RAS_AUTH_ATTRIBUTE, *PRAS_AUTH_ATTRIBUTE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasman.dll
api_name:
 - RasSecurityDialogGetInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Rasman.dll
req.irql: 
req.product: ADAM
---

# RasSecurityDialogGetInfo function


## -description


The 
<b>RasSecurityDialogGetInfo</b> function is called by a RAS security DLL to get information about a port from the RAS server.

To call this function, first call the 
<a href="_win32_loadlibrary">LoadLibrary</a> function to load Rasman.dll. Then call the 
<a href="_win32_getprocaddress">GetProcAddress</a> function to get the DLL's 
<b>RasSecurityDialogGetInfo</b> entry point.
<div class="alert"><b>Note</b>  Windows Server 2008, 
  Windows Server 2003,
  Windows 2000 Server, and
  Windows NT Server 4.0 currently provide RAS security host support for serial devices only. Other types of connections, such as Integrated Services Digital Network (ISDN) or virtual private network (VPN) connections, are not supported.</div><div> </div>

## -parameters




### -param hPort [in]

Specifies the port handle that the RAS server passed to the security DLL in the 
<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a> call for this authentication transaction.


### -param pBuffer [in]

Pointer to the 
<a href="https://msdn.microsoft.com/4bf5e0b8-087c-483b-a472-eab36840f554">RAS_SECURITY_INFO</a> structure that receives information about the specified RAS port.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the error codes defined in Raserror.h or Winerror.h. 
<a href="_win32_getlasterror">GetLastError</a> does not provide extended error information.




## -remarks



The 
<b>RasSecurityDialogGetInfo</b> function retrieves information about the port associated with a RAS security DLL authentication transaction.

The <b>LastError</b> member of the 
<a href="https://msdn.microsoft.com/4bf5e0b8-087c-483b-a472-eab36840f554">RAS_SECURITY_INFO</a> structure indicates the state of the last 
<a href="https://msdn.microsoft.com/ed5fcea6-6533-4c78-bd49-dfeaafd8192a">RasSecurityDialogReceive</a> call for the port. If the receive operation has been completed successfully, <b>LastError</b> is SUCCESS and the <b>BytesReceived</b> member indicates the number of bytes received. Otherwise, <b>LastError</b> is PENDING if the receive operation is still in progress, or a nonzero error code if the receive operation failed.




## -see-also




<a href="_win32_getprocaddress">GetProcAddress</a>



<a href="_win32_loadlibrary">LoadLibrary</a>



<a href="https://msdn.microsoft.com/44c000d7-2bb6-4fd8-ac5f-9d3850d857a0">RAS Server Administration Functions</a>



<a href="https://msdn.microsoft.com/4bf5e0b8-087c-483b-a472-eab36840f554">RAS_SECURITY_INFO</a>



<a href="https://msdn.microsoft.com/ed5fcea6-6533-4c78-bd49-dfeaafd8192a">RasSecurityDialogReceive</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>
 

 

