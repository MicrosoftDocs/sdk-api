---
UID: NF:certbcli.CertSrvBackupFree
title: CertSrvBackupFree function
author: windows-sdk-content
description: Used to free memory allocated from certain Certificate Services Backup APIs.
old-location: security\certsrvbackupfree.htm
tech.root: seccrypto
ms.assetid: dbfac3fc-3156-4253-812a-8b0647719096
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CertSrvBackupFree, CertSrvBackupFree function [Security], _certsrv_certsrvbackupfree, certbcli/CertSrvBackupFree, security.certsrvbackupfree
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
 - CertSrvBackupFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertSrvBackupFree function


## -description


The <b>CertSrvBackupFree</b> function is used to free memory allocated from certain Certificate Services Backup APIs.


## -parameters




### -param pv [in]

A pointer to the memory to be freed.


## -returns



This function does not return a value.




## -remarks



Call this function when finished with memory allocated by using the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376581(v=VS.85).aspx">CertSrvBackupGetBackupLogs</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376582(v=VS.85).aspx">CertSrvBackupGetDatabaseNames</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376583(v=VS.85).aspx">CertSrvBackupGetDynamicFileList</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377021(v=VS.85).aspx">CertSrvServerControl</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377003(v=VS.85).aspx">CertSrvRestoreGetDatabaseLocations</a>
</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNCERTSRVBACKUPFREE* pfnBackupFree;

char * szBackupFreeFunc = "CertSrvBackupFree";

// Get the address for the desired function.
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnBackupFree = (FNCERTSRVBACKUPFREE*)GetProcAddress(hInst,
                      szBackupFreeFunc);
if ( NULL == pfnBackupFree )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szBackupFreeFunc,
           GetLastError() );
    exit(1);
}

// Use the backup APIs.
// ...

// Free allocated memory.
// pBuff was allocated by another certsrv backup function.
pfnBackupFree(pBuff);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376581(v=VS.85).aspx">CertSrvBackupGetBackupLogs</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376582(v=VS.85).aspx">CertSrvBackupGetDatabaseNames</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376583(v=VS.85).aspx">CertSrvBackupGetDynamicFileList</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377003(v=VS.85).aspx">CertSrvRestoreGetDatabaseLocations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377021(v=VS.85).aspx">CertSrvServerControl</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa388174(v=VS.85).aspx">Using the Certificate Services Backup and Restore Functions</a>
 

 

