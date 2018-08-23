---
UID: NF:certbcli.CertSrvBackupTruncateLogs
title: CertSrvBackupTruncateLogs function
author: windows-sdk-content
description: Eliminates redundant records and reduces the disk storage space used by log files.
old-location: security\certsrvbackuptruncatelogs.htm
old-project: SecCrypto
ms.assetid: 8ccab63c-1057-485e-970e-8298dfea3426
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CertSrvBackupTruncateLogs, CertSrvBackupTruncateLogs function [Security], _certsrv_certsrvbackuptruncatelogs, certbcli/CertSrvBackupTruncateLogs, security.certsrvbackuptruncatelogs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: certbcli.h
req.include-header: Certsrv.h
req.redist: 
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
 - CertSrvBackupTruncateLogs
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# CertSrvBackupTruncateLogs function


## -description


The <b>CertSrvBackupTruncateLogs</b> function eliminates redundant records and reduces the disk storage space used by log files. Before truncating the log files, ensure that a backup of all files returned by 
<a href="https://msdn.microsoft.com/en-us/library/Aa376582(v=VS.85).aspx">CertSrvBackupGetDatabaseNames</a> and 
<a href="https://msdn.microsoft.com/en-us/library/Aa376581(v=VS.85).aspx">CertSrvBackupGetBackupLogs</a> have been secured.


## -parameters




### -param hbc [in]

A handle to a Certificate Services backup context.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -remarks



After securing a backup of the database and log files, the log files can optionally be truncated. Log file volume increases with database activity, and truncating the log files will reduce the redundant records in the log files (thereby decreasing the disk space used to store the log files).

The log files are provided for database integrity and efficiency. If a less-than-graceful exit occurs with the Certificate Services application, the next time Certificate Services is started, the database replays the log files to prevent data corruption from being introduced into the database.

Depending on the volume of the log files, the log file replay can be a time-consuming process. During this replay, the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> will be unavailable for other activity. Note that if the Certificate Services application is properly halted (such as by stopping the service or by shutting down the operating system properly), the log files are not replayed the next time it is started.

<div class="alert"><b>Note</b>  If you call <b>CertSrvBackupTruncateLogs</b> without backing up all files returned from 
<a href="https://msdn.microsoft.com/en-us/library/Aa376582(v=VS.85).aspx">CertSrvBackupGetDatabaseNames</a> and 
<a href="https://msdn.microsoft.com/en-us/library/Aa376581(v=VS.85).aspx">CertSrvBackupGetBackupLogs</a>, you will not be able to restore the backup set successfully, resulting in an unusable Certificate Services machine. Therefore, call <b>CertSrvBackupTruncateLogs</b> only when the backup set contains all files returned from 
<b>CertSrvBackupGetDatabaseNames</b> and 
<b>CertSrvBackupGetBackupLogs</b>.</div>
<div> </div>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNCERTSRVBACKUPTRUNCATELOGS* pfnTruncateLogs;
char * szTruncateLogsFunc = "CertSrvBackupTruncateLogs";

HRESULT    hr=0;

// Get the address for the desired function.
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnTruncateLogs = (FNCERTSRVBACKUPTRUNCATELOGS*)GetProcAddress( hInst,
                                           szTruncateLogsFunc );
if ( NULL == pfnTruncateLogs )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szTruncateLogsFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// After they have been backed up, truncate the logs.
// hCSBC is a previously set HCSBC variable.
hr = pfnTruncateLogs(hCSBC);
if (FAILED(hr))
{
    printf("Failed pfnTruncateLogs call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}
else
    printf("Logs truncated\n");</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376581(v=VS.85).aspx">CertSrvBackupGetBackupLogs</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa388174(v=VS.85).aspx">Using the Certificate Services Backup and Restore Functions</a>
 

 

