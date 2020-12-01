---
UID: NF:certbcli.CertSrvBackupGetDatabaseNamesW
title: CertSrvBackupGetDatabaseNamesW function (certbcli.h)
description: Retrieves the list of Certificate Services database file names that need to be backed up for the given backup context.
helpviewer_keywords: ["CSBFT_CERTSERVER_DATABASE","CertSrvBackupGetDatabaseNames","CertSrvBackupGetDatabaseNames function [Security]","CertSrvBackupGetDatabaseNamesW","_certsrv_certsrvbackupgetdatabasenames","certbcli/CertSrvBackupGetDatabaseNames","certbcli/CertSrvBackupGetDatabaseNamesW","security.certsrvbackupgetdatabasenames"]
old-location: security\certsrvbackupgetdatabasenames.htm
tech.root: security
ms.assetid: 5e62be79-693a-4543-8d83-262f00686c99
ms.date: 12/05/2018
ms.keywords: CSBFT_CERTSERVER_DATABASE, CertSrvBackupGetDatabaseNames, CertSrvBackupGetDatabaseNames function [Security], CertSrvBackupGetDatabaseNamesW, _certsrv_certsrvbackupgetdatabasenames, certbcli/CertSrvBackupGetDatabaseNames, certbcli/CertSrvBackupGetDatabaseNamesW, security.certsrvbackupgetdatabasenames
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertSrvBackupGetDatabaseNamesW
 - certbcli/CertSrvBackupGetDatabaseNamesW
dev_langs:
 - c++
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
---

# CertSrvBackupGetDatabaseNamesW function


## -description

The <b>CertSrvBackupGetDatabaseNames</b> function retrieves the list of Certificate Services database file names that need to be backed up for the given backup context.

## -parameters

### -param hbc [in]

A handle to a Certificate Services backup context.

### -param ppwszzAttachmentInformation [out]

A pointer to a <b>WCHAR</b> pointer that will receive the list of null-terminated database file names. There is a null character after every file name and an extra null character at the end of the list. The file name will be in the UNC form "## \\\\<i>Server</i>\\<i>SharePoint</i>\…<i>Path</i>…\\<i>FileName</i>.ext". The directory names will have the same form but without the trailing "\\<i>FileName</i>.ext". The text "##" denotes a Certificate Services Backup file type (CSBFT_*) and is stored as a single non-null <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> character prefixed onto each UNC path. The type tag is defined in Certbcli.h and can be the following value for this function. 




					

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
 

You must free this allocated memory when done by calling <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupfree">CertSrvBackupFree</a>. Before calling this function, setting *<i>ppwszzAttachmentInformation</i> to <b>NULL</b> is optional.

### -param pcbSize [out]

A pointer to the <b>DWORD</b> value that specifies the number of bytes in <i>ppwszzAttachmentInformation</i>.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -remarks

This function's name in the Certadm.dll is <b>CertSrvBackupGetDatabaseNamesW</b>. You must use this form of the name when calling <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVBACKUPGETDATABASENAMESW</b> in the Certbcli.h header file.


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

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupfree">CertSrvBackupFree</a>



<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupopenfilew">CertSrvBackupOpenFile</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>