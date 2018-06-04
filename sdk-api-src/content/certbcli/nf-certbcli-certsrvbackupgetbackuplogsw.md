---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CertSrvBackupGetBackupLogsW function


## -description



			The <b>CertSrvBackupGetBackupLogs</b> function retrieves the list of Certificate Services log file names that need to be backed up for the given backup context.


## -parameters




### -param hbc [in]

A handle to a Certificate Services backup context.


### -param ppwszzBackupLogFiles [out]

A pointer to <b>WCHAR</b> pointer that will receive the list of null-terminated log file names. There is a null character after every file name and an extra null character at the end of the list. The file name will be in the UNC form "## \\<i>Server</i>\<i>SharePoint</i>\…<i>Path</i>…\<i>FileName</i>.ext". The directory names will have the same form but without the trailing "\<i>FileName</i>.ext". The text "##" denotes a Certificate Services Backup file type (CSBFT_*) and is stored as a single non-null <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> character prefixed onto each UNC path. This type tag is defined in Certbcli.h and can be one of the following values for this function.

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
 

When you have finished using this allocated memory, free it by calling the <a href="https://msdn.microsoft.com/dbfac3fc-3156-4253-812a-8b0647719096">CertSrvBackupFree</a> function.

Setting <i>ppwszzBackupLogFiles</i> to <b>NULL</b> before calling this function is optional.


### -param pcbSize [out]

A pointer to the <b>DWORD</b> value that specifies the number of bytes in <i>ppwszzBackupLogFiles</i>.


## -returns




						The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates success.




## -remarks



The log files represent database activity (request submissions, certificate revocation, and so on) that has occurred since the last log file truncation. Log file volume increases as database activity occurs. The log files can be decreased in size by performing a backup and then calling 
<a href="https://msdn.microsoft.com/8ccab63c-1057-485e-970e-8298dfea3426">CertSrvBackupTruncateLogs</a>.

This function's name in the Certadm.dll is <b>CertSrvBackupGetBackupLogsW</b>. You must use this form of the name when calling <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVBACKUPGETBACKUPLOGSW</b> in the Certbcli.h header file.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNCERTSRVBACKUPGETBACKUPLOGSW* pfnGetBackupLogs;
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
hr = pfnGetBackupLogs(hCSBC, &amp;pwszzLogFiles, &amp;nListBytes);
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
        printf("%02x: %ws\n", *pwszLog, &amp;pwszLog[1]);
        // Move to the next logfile name.
        // + 1 moves past the null terminator.
        pwszLog+=(wcslen(pwszLog)) + 1; 
    }

    // Free the allocated memory.
    // pfnBackupFree is the address of the CertSrvBackupFree
	   // function.
    pfnBackupFree(pwszzLogFiles);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dbfac3fc-3156-4253-812a-8b0647719096">CertSrvBackupFree</a>



<a href="https://msdn.microsoft.com/5ddce73f-c693-437a-9eae-d7eaf482ee05">CertSrvBackupOpenFile</a>



<a href="https://msdn.microsoft.com/8ccab63c-1057-485e-970e-8298dfea3426">CertSrvBackupTruncateLogs</a>



<a href="https://msdn.microsoft.com/47e8f490-ecb2-4c41-8bf0-b673e173ddc6">Using the Certificate Services Backup and Restore Functions</a>
 

 

