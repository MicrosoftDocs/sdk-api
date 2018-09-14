---
UID: NF:certbcli.CertSrvBackupEnd
title: CertSrvBackupEnd function
author: windows-sdk-content
description: Ends a Certificate Services backup session.
old-location: security\certsrvbackupend.htm
tech.root: seccrypto
ms.assetid: ebf87af3-df45-4440-9881-e2926b0c4f08
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CertSrvBackupEnd, CertSrvBackupEnd function [Security], _certsrv_certsrvbackupend, certbcli/CertSrvBackupEnd, security.certsrvbackupend
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
req.unicode-ansi: 
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
 - CertSrvBackupEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertSrvBackupEnd function


## -description


The <b>CertSrvBackupEnd</b> function ends a Certificate Services backup session.


## -parameters




### -param hbc [in]

A handle to a Certificate Services backup context.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -remarks



Upon completion of a backup session, the session needs to be terminated by means of <b>CertSrvBackupEnd</b>. For every successful call to <a href="https://msdn.microsoft.com/21af96f8-168d-4c6c-8966-357236c0e4e6">CertSrvBackupPrepare</a>, there should be a call to <b>CertSrvBackupEnd</b>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNCERTSRVBACKUPEND* pfnBackupEnd;
char * szBackEndFunc = "CertSrvBackupEnd";
HRESULT    hr=0;

// Get the address for the desired function.
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnBackupEnd = (FNCERTSRVBACKUPEND*)GetProcAddress(hInst,
                                       szBackEndFunc);
if (NULL == pfnBackupEnd)
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szBackEndFunc,
           GetLastError() );
    exit(1);  // Or other appropriate error action.
}

// When done, release the HCSBC.
// hCSBC would have been created by an earlier call
// to CertSrvBackupPrepare.
hr = pfnBackupEnd(hCSBC);
if (FAILED(hr))
{
    printf("Failed pfnBackupEnd call [%x]\n", hr);
    exit(1);  // Or other appropriate error action.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/21af96f8-168d-4c6c-8966-357236c0e4e6">CertSrvBackupPrepare</a>



<a href="https://msdn.microsoft.com/47e8f490-ecb2-4c41-8bf0-b673e173ddc6">Using the Certificate Services Backup and Restore Functions</a>
 

 

