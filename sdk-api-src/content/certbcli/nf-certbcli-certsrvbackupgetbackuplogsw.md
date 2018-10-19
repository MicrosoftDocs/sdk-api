---
UID: NF:certbcli.CertSrvBackupGetBackupLogsW
title: CertSrvBackupGetBackupLogsW function
author: windows-sdk-content
description: Retrieves the list of Certificate Services log file names that need to be backed up for the given backup context.
old-location: security\certsrvbackupgetbackuplogs.htm
tech.root: seccrypto
ms.assetid: bbc6e6c2-bb2c-4b0e-b1ba-6acf26a48f45
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CSBFT_LOG, CSBFT_PATCH_FILE, CertSrvBackupGetBackupLogs, CertSrvBackupGetBackupLogs function [Security], CertSrvBackupGetBackupLogsW, _certsrv_certsrvbackupgetbackuplogs, certbcli/CertSrvBackupGetBackupLogs, certbcli/CertSrvBackupGetBackupLogsW, security.certsrvbackupgetbackuplogs
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
req.unicode-ansi: CertSrvBackupGetBackupLogsW (Unicode)
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
 - CertSrvBackupGetBackupLogs
 - CertSrvBackupGetBackupLogsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertSrvBackupGetBackupLogsW function


## -description


The <b>CertSrvBackupGetBackupLogs</b> function retrieves the list of Certificate Services log file names that need to be backed up for the given backup context.


## -parameters




### -param hbc [in]

A handle to a Certificate Services backup context.


### -param ppwszzBackupLogFiles [out]

A pointer to <b>WCHAR</b> pointer that will receive the list of null-terminated log file names. There is a null character after every file name and an extra null character at the end of the list. The file name will be in the UNC form "## \\<i>Server</i>\<i>SharePoint</i>\…<i>Path</i>…\<i>FileName</i>.ext". The directory names will have the same form but without the trailing "\<i>FileName</i>.ext". The text "##" denotes a Certificate Services Backup file type (CSBFT_*) and is stored as a single non-null <a href="https://msdn.microsoft.com/en-us/library/ms721629(v=VS.85).aspx">Unicode</a> character prefixed onto each UNC path. This type tag is defined in Certbcli.h and can be one of the following values for this function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CSBFT_LOG"></a><a id="csbft_log"></a><dl>
<dt><b>CSBFT_LOG</b></dt>
</dl>
</td>
<td width="60%">
Certificate Services database log file name including path.

</td>
</tr>
<tr>
<td width="40%"><a id="CSBFT_PATCH_FILE"></a><a id="csbft_patch_file"></a><dl>
<dt><b>CSBFT_PATCH_FILE</b></dt>
</dl>
</td>
<td width="60%">
The name, including path, of the update file for the Certificate Services database.

<b>Windows Server 2003:  </b>Database update files are not used.

</td>
</tr>
</table>
 

When you have finished using this allocated memory, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa376580(v=VS.85).aspx">CertSrvBackupFree</a> function.

Setting <i>ppwszzBackupLogFiles</i> to <b>NULL</b> before calling this function is optional.


### -param pcbSize [out]

A pointer to the <b>DWORD</b> value that specifies the number of bytes in <i>ppwszzBackupLogFiles</i>.


## -returns



The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates success.




## -remarks



The log files represent database activity (request submissions, certificate revocation, and so on) that has occurred since the last log file truncation. Log file volume increases as database activity occurs. The log files can be decreased in size by performing a backup and then calling 
<a href="https://msdn.microsoft.com/en-us/library/Aa376587(v=VS.85).aspx">CertSrvBackupTruncateLogs</a>.

This function's name in the Certadm.dll is <b>CertSrvBackupGetBackupLogsW</b>. You must use this form of the name when calling <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVBACKUPGETBACKUPLOGSW</b> in the Certbcli.h header file.


#### Examples


```cpp
FNCERTSRVBACKUPGETBACKUPLOGSW* pfnGetBackupLogs;
char * szGetBackupLogsFunc = "CertSrvBackupGetBackupLogsW";

WCHAR *    pwszzLogFiles;

DWORD      nListBytes=0;

HRESULT    hr=0;

// Get the address for the desired function.
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnGetBackupLogs = (FNCERTSRVBACKUPGETBACKUPLOGSW*)GetProcAddress
    (hInst, szGetBackupLogsFunc);
if ( NULL == pfnGetBackupLogs )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szGetBackupLogsFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// Determine the names of the log files.
// hCSBC was set by an earlier call to CertSrvbackupPrepare.
hr = pfnGetBackupLogs(hCSBC, &pwszzLogFiles, &nListBytes);
if (FAILED(hr))
{
    printf("Failed pfnGetBackupLogs call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}
else
{
    printf("%d bytes for log file names\n", nListBytes);
    WCHAR * pwszLog = pwszzLogFiles;
    // Process the list.
    while ( L'\0' != *pwszLog )
    {
        // Use the file name referenced by pwszLog.
        // Here it is merely displayed.
        printf("%02x: %ws\n", *pwszLog, &pwszLog[1]);
        // Move to the next logfile name.
        // + 1 moves past the null terminator.
        pwszLog+=(wcslen(pwszLog)) + 1; 
    }

    // Free the allocated memory.
    // pfnBackupFree is the address of the CertSrvBackupFree
	   // function.
    pfnBackupFree(pwszzLogFiles);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376580(v=VS.85).aspx">CertSrvBackupFree</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376584(v=VS.85).aspx">CertSrvBackupOpenFile</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376587(v=VS.85).aspx">CertSrvBackupTruncateLogs</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa388174(v=VS.85).aspx">Using the Certificate Services Backup and Restore Functions</a>
 

 

