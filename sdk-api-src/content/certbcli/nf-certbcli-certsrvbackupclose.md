---
UID: NF:certbcli.CertSrvBackupClose
title: CertSrvBackupClose function
author: windows-sdk-content
description: Closes the file opened by the CertSrvBackupOpenFile function.
old-location: security\certsrvbackupclose.htm
old-project: seccrypto
ms.assetid: 123933b4-5496-460d-aaaa-a494786cd638
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CertSrvBackupClose, CertSrvBackupClose function [Security], _certsrv_certsrvbackupclose, certbcli/CertSrvBackupClose, security.certsrvbackupclose
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Certadm.dll
api_name:
 - CertSrvBackupClose
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# CertSrvBackupClose function


## -description


The <b>CertSrvBackupClose</b>  function closes the file opened by the 
<a href="https://msdn.microsoft.com/5ddce73f-c693-437a-9eae-d7eaf482ee05">CertSrvBackupOpenFile</a> function.


## -parameters




### -param hbc [in]

A handle to a Certificate Services backup context.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -remarks



For every successful call to <a href="https://msdn.microsoft.com/5ddce73f-c693-437a-9eae-d7eaf482ee05">CertSrvBackupOpenFile</a>, there should be a subsequent call to <b>CertSrvBackupClose</b>. Upon completion of backing up a  file, the file needs to be closed.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNCERTSRVBACKUPCLOSE* pfnClose;
char * szBackupCloseFunc = "CertSrvBackupClose";
HRESULT    hr=0;

// Get the address for the desired function.    
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnClose = (FNCERTSRVBACKUPCLOSE*)GetProcAddress(hInst,
                                   szBackupCloseFunc);
if ( NULL == pfnClose )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
            szBackupCloseFunc,
            GetLastError() );
    exit(1);  // Or other appropriate error action.
}
// Close the file.
// hCSBC represents an HCSBC used in
// an earlier call to CertSrvBackupOpenFile.
hr = pfnClose(hCSBC);
if (FAILED(hr))
{
    printf("Failed pfnClose call [%x]\n", hr);
    exit(1);  // Or other appropriate error action.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5ddce73f-c693-437a-9eae-d7eaf482ee05">CertSrvBackupOpenFile</a>



<a href="https://msdn.microsoft.com/cfc72002-40ee-4854-a026-b956acd5d758">CertSrvBackupRead</a>



<a href="https://msdn.microsoft.com/47e8f490-ecb2-4c41-8bf0-b673e173ddc6">Using the Certificate Services Backup and Restore Functions</a>
 

 

