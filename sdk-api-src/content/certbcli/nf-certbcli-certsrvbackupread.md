---
UID: NF:certbcli.CertSrvBackupRead
title: CertSrvBackupRead function
author: windows-sdk-content
description: Reads bytes from a Certificate Services file.
old-location: security\certsrvbackupread.htm
tech.root: seccrypto
ms.assetid: cfc72002-40ee-4854-a026-b956acd5d758
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CertSrvBackupRead, CertSrvBackupRead function [Security], _certsrv_certsrvbackupread, certbcli/CertSrvBackupRead, security.certsrvbackupread
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
 - CertSrvBackupRead
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertSrvBackupRead function


## -description


The <b>CertSrvBackupRead</b> function reads bytes from a Certificate Services file.


## -parameters




### -param hbc [in]

A handle to a Certificate Services backup context.


### -param pvBuffer [out]

Void pointer to storage which will contain bytes read from the file being backed up.


### -param cbBuffer [in]

Size of the storage area referenced by <i>pvBuffer</i>.


### -param pcbRead [out]

A pointer to a <b>DWORD</b> value which represents the actual number of bytes read by <b>CertSrvBackupRead</b>. The number of bytes read can be less than the size of the storage area allocated to <i>pvBuffer</i> if the end of the file has been reached.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -remarks



After opening the file for backup purposes (using 
<a href="https://msdn.microsoft.com/5ddce73f-c693-437a-9eae-d7eaf482ee05">CertSrvBackupOpenFile</a>), call <b>CertSrvBackupRead</b> to retrieve the contents of the file, and call an application-specific routine to write the contents to a backup medium. <b>CertSrvBackupRead</b> and the application-specific routine can be placed in a loop until all the bytes of the file are read and backed up. When done reading the file, close it by calling 
<a href="https://msdn.microsoft.com/123933b4-5496-460d-aaaa-a494786cd638">CertSrvBackupClose</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;Certbcli.h&gt;

#define BUFFSIZE 524288

FNCERTSRVBACKUPREAD* pfnRead;
char * szBackupReadFunc = "CertSrvBackupRead";
BYTE       ReadBuff[BUFFSIZE];
DWORD      cbRead=0;
HRESULT    hr=0;

// Get the address for the desired function.    
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnRead = (FNCERTSRVBACKUPREAD*)GetProcAddress(hInst,
                                          szBackupReadFunc);
if ( NULL == pfnRead )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szBackupReadFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// Read the file.
// hCSBC represents an HCSBC used in
// an earlier call to CertSrvBackupOpenFile.
// To read the entire file, this code
// would be placed in a loop.
hr = pfnRead( hCSBC,
              &amp;ReadBuff,
              BUFFSIZE,
              &amp;cbRead );
if (FAILED(hr))
{
    printf("Failed pfnRead call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}

// Use the bytes read as needed. For example,
// in an application-specific routine to back
// up the file contents.
// ...</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/123933b4-5496-460d-aaaa-a494786cd638">CertSrvBackupClose</a>



<a href="https://msdn.microsoft.com/5ddce73f-c693-437a-9eae-d7eaf482ee05">CertSrvBackupOpenFile</a>



<a href="https://msdn.microsoft.com/47e8f490-ecb2-4c41-8bf0-b673e173ddc6">Using the Certificate Services Backup and Restore Functions</a>
 

 

