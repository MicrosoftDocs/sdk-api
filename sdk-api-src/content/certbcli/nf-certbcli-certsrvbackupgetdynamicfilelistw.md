---
UID: NF:certbcli.CertSrvBackupGetDynamicFileListW
title: CertSrvBackupGetDynamicFileListW function
author: windows-sdk-content
description: Retrieves the list of Certificate Services dynamic file names that need to be backed up for the given backup context.
old-location: security\certsrvbackupgetdynamicfilelist.htm
tech.root: seccrypto
ms.assetid: ff60b705-5ac6-4e61-9b88-9ffc2dc9adce
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CertSrvBackupGetDynamicFileList, CertSrvBackupGetDynamicFileList function [Security], CertSrvBackupGetDynamicFileListW, _certsrv_certsrvbackupgetdynamicfilelist, certbcli/CertSrvBackupGetDynamicFileList, certbcli/CertSrvBackupGetDynamicFileListW, security.certsrvbackupgetdynamicfilelist
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
req.unicode-ansi: CertSrvBackupGetDynamicFileListW (Unicode)
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
 - CertSrvBackupGetDynamicFileList
 - CertSrvBackupGetDynamicFileListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertSrvBackupGetDynamicFileListW function


## -description


The <b>CertSrvBackupGetDynamicFileList</b> function retrieves the list of Certificate Services dynamic file names that need to be backed up for the given backup context. The dynamic files are those that are not included in the Certificate Services database backup.


## -parameters




### -param hbc [in]

A handle to a Certificate Services backup context.


### -param ppwszzFileList [out]

A pointer to a <b>WCHAR</b> pointer that will receive the list of null-terminated dynamic file names used by Certificate Services. There is a null character after every file name and an extra null character at the end of the list. The file name will be in the UNC form "\\<i>Server</i>\<i>SharePoint</i>\…<i>Path</i>…\<i>FileName</i>.ext". When you have finished using this allocated memory, free it by calling the <a href="https://msdn.microsoft.com/dbfac3fc-3156-4253-812a-8b0647719096">CertSrvBackupFree</a> function.

Before calling this function, setting *<i>ppwszzFileList</i> to <b>NULL</b> is optional.


### -param pcbSize [out]

A pointer to the <b>DWORD</b> value that specifies the number of bytes in <i>ppwszzFileList</i>.


## -returns



The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates success.




## -remarks



Use this function to retrieve a list of the Certificate Services dynamic file names. These files are separate from the Certificate Services database and log files, and they are not backed up by the Certificate Services backup APIs. As a result, some other means must be used to back up the dynamic files. An example of a Certificate Services dynamic file is the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL).

This function's name in the Certadm.dll is <b>CertSrvBackupGetDynamicFileListW</b>. You must use this form of the name when calling <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVBACKUPGETDYNAMICFILELISTW</b> in the Certbcli.h header file.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNCERTSRVBACKUPGETDYNAMICFILELISTW* pfnGetDynFiles;
char * szGetDynFilesFunc = "CertSrvBackupGetDynamicFileListW";
WCHAR *    pwszzDynFiles;
DWORD      nListBytes=0;
HRESULT    hr=0;

// Get the address for the desired function.    
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnGetDynFiles = (FNCERTSRVBACKUPGETDYNAMICFILELISTW*)
    GetProcAddress(hInst, szGetDynFilesFunc);
if ( NULL == pfnGetDynFiles )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szGetDynFilesFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// Determine the names of the dynamic files.
// hCSBC was set by an earlier call to CertSrvBackupPrepare.
hr = pfnGetDynFiles(hCSBC, &amp;pwszzDynFiles, &amp;nListBytes);
if (FAILED(hr))
{
    printf("Failed pfnGetDynFiles call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}
else
{
    printf("%d bytes for dynamic file names\n", nListBytes);
    WCHAR * pwszFile = pwszzDynFiles;
    // Process the list.
    while ( L'\0' != *pwszFile )
    {
        // Use the file name referenced by pwszFile.
        // Here it is merely displayed.
        printf("%ws\n", pwszFile);
        // Move to the next dynamic file name.
        // + 1 moves past the null terminator.
        pwszFile+=(wcslen(pwszFile)) + 1; 
    }
    // Free the allocated memory.
    // pfnBackupFree is the address of the 
    // CertSrvBackupFree function.
    pfnBackupFree(pwszzDynFiles);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dbfac3fc-3156-4253-812a-8b0647719096">CertSrvBackupFree</a>



<a href="https://msdn.microsoft.com/47e8f490-ecb2-4c41-8bf0-b673e173ddc6">Using the Certificate Services Backup and Restore Functions</a>
 

 

