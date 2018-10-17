---
UID: NF:certbcli.CertSrvServerControlW
title: CertSrvServerControlW function
author: windows-sdk-content
description: Issues a service control command to programmatically stop Certificate Services.
old-location: security\certsrvservercontrol.htm
tech.root: seccrypto
ms.assetid: 6f32e7f4-60d5-4370-b240-46aa2475e279
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: CSCONTROL_SHUTDOWN, CertSrvServerControl, CertSrvServerControl function [Security], CertSrvServerControlW, _certsrv_certsrvservercontrol, certbcli/CertSrvServerControl, certbcli/CertSrvServerControlW, security.certsrvservercontrol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: certbcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertSrvServerControlW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Certadm.dll
api_name:
 - CertSrvServerControl
 - CertSrvServerControlW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertSrvServerControlW function


## -description


The <b>CertSrvServerControl</b>  function issues a service control command to programmatically stop Certificate Services.


## -parameters




### -param pwszServerName [in]

A pointer to a name or a configuration string of the server to be issued the control command.


### -param dwControlFlags [in]

Value representing the control command being issued to the Certificate Services server specified by <i>pwszServerName</i>. The following value is supported for <i>dwControlFlags</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CSCONTROL_SHUTDOWN"></a><a id="cscontrol_shutdown"></a><dl>
<dt><b>CSCONTROL_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
Stop Certificate Services.

</td>
</tr>
</table>
 


### -param pcbOut [out]

For future use, this parameter will be the number of bytes allocated to <i>ppbOut</i>. The current implementation does not allocate memory to <i>ppbOut</i>. You can set this value to <b>NULL</b>.


### -param ppbOut [out]

For future use, this parameter will be the pointer to pointer to bytes representing the output from the issued command. The current implementation does not allocate memory to <i>ppbOut</i>. You can set this value to <b>NULL</b>.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -remarks



The purpose of this function is to allow a backup or restore application to programmatically stop the Certificate Services application (thereby not requiring the use of the service controller APIs). Stopping Certificate Services in this manner will also work when Certificate Services is running in console mode; the service controller APIs cannot control applications running in console mode.

This function's name in Certadm.dll is <b>CertSrvServerControlW</b>. You must use this form of the name when calling <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVSERVERCONTROLW</b> in the Certbcli.h header file.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNCERTSRVSERVERCONTROLW* pfnControl;
char * szControlFunc = "CertSrvServerControlW";
HRESULT    hr=0;

// Get the address for the desired function.
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnControl = (FNCERTSRVSERVERCONTROLW*)GetProcAddress(hInst,
                                           szControlFunc);
if ( NULL == pfnControl )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szControlFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// Issue a command to stop the service.
hr = pfnControl( L"MyCertServMachine",
                 CSCONTROL_SHUTDOWN,
                 NULL,
                 NULL);

if ( FAILED( hr ) )
{
    printf("Failed pfnControl call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/47e8f490-ecb2-4c41-8bf0-b673e173ddc6">Using the Certificate Services Backup and Restore Functions</a>
 

 

