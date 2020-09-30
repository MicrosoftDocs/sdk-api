---
UID: NF:certbcli.CertSrvRestoreGetDatabaseLocationsW
title: CertSrvRestoreGetDatabaseLocationsW function (certbcli.h)
description: Used both in backup and restore scenarios and retrieves the list of Certificate Services database location names for all the files being backed up or restored.
helpviewer_keywords: ["CSBFT_CERTSERVER_DATABASE","CSBFT_CHECKPOINT_DIR","CSBFT_LOG_DIR","CertSrvRestoreGetDatabaseLocations","CertSrvRestoreGetDatabaseLocations function [Security]","CertSrvRestoreGetDatabaseLocationsW","_certsrv_certsrvrestoregetdatabaselocations","certbcli/CertSrvRestoreGetDatabaseLocations","certbcli/CertSrvRestoreGetDatabaseLocationsW","security.certsrvrestoregetdatabaselocations"]
old-location: security\certsrvrestoregetdatabaselocations.htm
tech.root: security
ms.assetid: 02355bd7-6788-4c32-940e-b89e47619aa0
ms.date: 12/05/2018
ms.keywords: CSBFT_CERTSERVER_DATABASE, CSBFT_CHECKPOINT_DIR, CSBFT_LOG_DIR, CertSrvRestoreGetDatabaseLocations, CertSrvRestoreGetDatabaseLocations function [Security], CertSrvRestoreGetDatabaseLocationsW, _certsrv_certsrvrestoregetdatabaselocations, certbcli/CertSrvRestoreGetDatabaseLocations, certbcli/CertSrvRestoreGetDatabaseLocationsW, security.certsrvrestoregetdatabaselocations
req.header: certbcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertSrvRestoreGetDatabaseLocationsW (Unicode)
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
 - CertSrvRestoreGetDatabaseLocationsW
 - certbcli/CertSrvRestoreGetDatabaseLocationsW
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
 - CertSrvRestoreGetDatabaseLocations
 - CertSrvRestoreGetDatabaseLocationsW
---

# CertSrvRestoreGetDatabaseLocationsW function


## -description

The <b>CertSrvRestoreGetDatabaseLocations</b> function is used both in backup and restore scenarios and retrieves the list of Certificate Services database location names for all the files being backed up or restored.

## -parameters

### -param hbc [in]

A handle to a Certificate Services backup or restore context.

### -param ppwszzDatabaseLocationList [out]

A pointer to a <b>WCHAR</b> pointer to receive the list of null-terminated database location names, log directory name, and system (or checkpoint) directory name. There is a null character after every name and an extra null character at the end of the list. The location name will be in the UNC form "## &#92;&#92;<i>Server</i>&#92;<i>SharePoint</i>\…<i>Path</i>…&#92;<i>FileName</i>.ext". The directory names will have the same form but without the trailing "&#92;<i>FileName</i>.ext". The text "##" denotes a Certificate Services Backup file type (CSBFT_*) and is stored as a single non-null <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> character prefixed onto each UNC path. The type tag is defined in Certbcli.h and can be one of the following values for this function.

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
<tr>
<td width="40%"><a id="CSBFT_CHECKPOINT_DIR"></a><a id="csbft_checkpoint_dir"></a><dl>
<dt><b>CSBFT_CHECKPOINT_DIR</b></dt>
</dl>
</td>
<td width="60%">
Certificate Services database system (or checkpoint) directory.

</td>
</tr>
<tr>
<td width="40%"><a id="CSBFT_LOG_DIR"></a><a id="csbft_log_dir"></a><dl>
<dt><b>CSBFT_LOG_DIR</b></dt>
</dl>
</td>
<td width="60%">
Certificate Services database log directory.

</td>
</tr>
</table>
 

You must free this allocated memory when done by calling <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupfree">CertSrvBackupFree</a>.

Setting *<i>ppwszzDatabaseLocationList</i> to <b>NULL</b> before calling this function is optional.

### -param pcbSize [out]

A pointer to the <b>DWORD</b> value that specifies the number of bytes in <i>ppwszzDatabaseLocationList</i>.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -remarks

Certificate Services must be running for this method to succeed.

This function's name in Certadm.dll is <b>CertSrvRestoreGetDatabaseLocationsW</b>. You must use this form of the name when calling <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVRESTOREGETDATABASELOCATIONSW</b> in the Certbcli.h header file.


#### Examples


```cpp
FNCERTSRVRESTOREGETDATABASELOCATIONSW* pfnGetDBLocs;
char *  szGetDBLocsFunc = "CertSrvRestoreGetDatabaseLocationsW";
WCHAR * pwszzDBLocs;
DWORD   nListBytes=0;
HRESULT hr=0;

// Get the address for the desired function.    
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnGetDBLocs = (FNCERTSRVRESTOREGETDATABASELOCATIONSW*)
    GetProcAddress(hInst, szGetDBLocsFunc);
if ( NULL == pfnGetDBLocs )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szGetDBLocsFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// Determine the names of the database locations.
// hCSBC was set by an earlier call to CertSrvRestorePrepare.
hr = pfnGetDBLocs(hCSBC, &pwszzDBLocs, &nListBytes);
if (FAILED(hr))
{
    printf("Failed pfnGetDBLocs call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}
else
{
    printf("%d bytes for DB locations\n", nListBytes);
    WCHAR * pwszFile = pwszzDBLocs;
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
    pfnBackupFree(pwszzDBLocs);
}
```

## -see-also

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupfree">CertSrvBackupFree</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>