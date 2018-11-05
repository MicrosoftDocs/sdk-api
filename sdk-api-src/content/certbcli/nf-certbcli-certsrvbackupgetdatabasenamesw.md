---
UID: NF:certbcli.CertSrvBackupGetDatabaseNamesW
title: CertSrvBackupGetDatabaseNamesW function
author: windows-sdk-content
description: Retrieves the list of Certificate Services database file names that need to be backed up for the given backup context.
old-location: security\certsrvbackupgetdatabasenames.htm
tech.root: seccrypto
ms.assetid: 5e62be79-693a-4543-8d83-262f00686c99
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CSBFT_CERTSERVER_DATABASE, CertSrvBackupGetDatabaseNames, CertSrvBackupGetDatabaseNames function [Security], CertSrvBackupGetDatabaseNamesW, _certsrv_certsrvbackupgetdatabasenames, certbcli/CertSrvBackupGetDatabaseNames, certbcli/CertSrvBackupGetDatabaseNamesW, security.certsrvbackupgetdatabasenames
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
req.unicode-ansi: CertSrvBackupGetDatabaseNamesW (Unicode)
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
 - CertSrvBackupGetDatabaseNames
 - CertSrvBackupGetDatabaseNamesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertSrvBackupGetDatabaseNamesW function


## -description


The <b>CertSrvBackupGetDatabaseNames</b> function retrieves the list of Certificate Services database file names that need to be backed up for the given backup context.


## -parameters




### -param hbc [in]

A handle to a Certificate Services backup context.


### -param ppwszzAttachmentInformation [out]

A pointer to a <b>WCHAR</b> pointer that will receive the list of null-terminated database file names. There is a null character after every file name and an extra null character at the end of the list. The file name will be in the UNC form "## \\<i>Server</i>\<i>SharePoint</i>\…<i>Path</i>…\<i>FileName</i>.ext". The directory names will have the same form but without the trailing "\<i>FileName</i>.ext". The text "##" denotes a Certificate Services Backup file type (CSBFT_*) and is stored as a single non-null <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> character prefixed onto each UNC path. The type tag is defined in Certbcli.h and can be the following value for this function. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CSBFT_CERTSERVER_DATABASE"></a><a id="csbft_certserver_database"></a><dl>
<dt><b>CSBFT_CERTSERVER_DATABASE</b></dt>
</dl>
</td>
<td width="60%">
Certificate Services database file name including path.

</td>
</tr>
</table>
 

You must free this allocated memory when done by calling <a href="https://msdn.microsoft.com/dbfac3fc-3156-4253-812a-8b0647719096">CertSrvBackupFree</a>. Before calling this function, setting *<i>ppwszzAttachmentInformation</i> to <b>NULL</b> is optional.


### -param pcbSize [out]

A pointer to the <b>DWORD</b> value that specifies the number of bytes in <i>ppwszzAttachmentInformation</i>.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -remarks



This function's name in the Certadm.dll is <b>CertSrvBackupGetDatabaseNamesW</b>. You must use this form of the name when calling <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVBACKUPGETDATABASENAMESW</b> in the Certbcli.h header file.


#### Examples


```cpp
FNCERTSRVBACKUPGETDATABASENAMESW* pfnGetDBNames;
char * szGetDBNamesFunc = "CertSrvBackupGetDatabaseNamesW";
WCHAR *    pwszzDBFiles;
DWORD      nListBytes=0;
HRESULT    hr=0;

// Get the address for the desired function.    
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnGetDBNames = (FNCERTSRVBACKUPGETDATABASENAMESW*)
    GetProcAddress(hInst, szGetDBNamesFunc);

if ( NULL == pfnGetDBNames )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szGetDBNamesFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// Determine the names of the database files.
// hCSBC was set by an earlier call to CertSrvBackupPrepare
hr = pfnGetDBNames(hCSBC, &pwszzDBFiles, &nListBytes);
if (FAILED(hr))
{
    printf("Failed pfnGetDBNames call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}
else
{
    printf("%d bytes for DB file names\n", nListBytes);
    WCHAR * pwszFile = pwszzDBFiles;
    // Process the list.
    while ( L'\0' != *pwszFile )
    {
        // Use the file name referenced by pwszFile.
        // Here it is merely displayed.
        printf("%02x: %ws\n", *pwszFile, &pwszFile[1]);
        // Move to the next database file name.
        // + 1 moves past the null terminator.
        pwszFile+=(wcslen(pwszFile)) + 1; 
    }
    // Free the allocated memory.
    // pfnBackupFree is the address of the 
    // CertSrvBackupFree function.
    pfnBackupFree(pwszzDBFiles);
}
```





## -see-also




<a href="https://msdn.microsoft.com/dbfac3fc-3156-4253-812a-8b0647719096">CertSrvBackupFree</a>



<a href="https://msdn.microsoft.com/5ddce73f-c693-437a-9eae-d7eaf482ee05">CertSrvBackupOpenFile</a>



<a href="https://msdn.microsoft.com/47e8f490-ecb2-4c41-8bf0-b673e173ddc6">Using the Certificate Services Backup and Restore Functions</a>
 

 

