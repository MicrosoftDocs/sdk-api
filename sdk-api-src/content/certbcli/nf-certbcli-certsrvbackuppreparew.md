---
UID: NF:certbcli.CertSrvBackupPrepareW
title: CertSrvBackupPrepareW function (certbcli.h)
description: Used to prepare a Certificate Services server for backup operations.
helpviewer_keywords: ["CSBACKUP_TYPE_FULL","CSBACKUP_TYPE_LOGS_ONLY","CertSrvBackupPrepare","CertSrvBackupPrepare function [Security]","CertSrvBackupPrepareW","_certsrv_certsrvbackupprepare","certbcli/CertSrvBackupPrepare","certbcli/CertSrvBackupPrepareW","security.certsrvbackupprepare"]
old-location: security\certsrvbackupprepare.htm
tech.root: security
ms.assetid: 21af96f8-168d-4c6c-8966-357236c0e4e6
ms.date: 12/05/2018
ms.keywords: CSBACKUP_TYPE_FULL, CSBACKUP_TYPE_LOGS_ONLY, CertSrvBackupPrepare, CertSrvBackupPrepare function [Security], CertSrvBackupPrepareW, _certsrv_certsrvbackupprepare, certbcli/CertSrvBackupPrepare, certbcli/CertSrvBackupPrepareW, security.certsrvbackupprepare
req.header: certbcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertSrvBackupPrepareW (Unicode)
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
 - CertSrvBackupPrepareW
 - certbcli/CertSrvBackupPrepareW
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
 - CertSrvBackupPrepare
 - CertSrvBackupPrepareW
---

# CertSrvBackupPrepareW function


## -description

The <b>CertSrvBackupPrepare</b> function is used to prepare a Certificate Services server for backup operations.

## -parameters

### -param pwszServerName [in]

A pointer to the machine name of the server to prepare for online backup. This name can be the NetBIOS name or the DNS name.

### -param grbitJet [in]

Value used by the database engine; this value should be set to zero.

### -param dwBackupFlags [in]

Specifies the backup type. This can be either of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CSBACKUP_TYPE_FULL"></a><a id="csbackup_type_full"></a><dl>
<dt><b>CSBACKUP_TYPE_FULL</b></dt>
</dl>
</td>
<td width="60%">
Backup the Certificate Services database, logs and related files.

</td>
</tr>
<tr>
<td width="40%"><a id="CSBACKUP_TYPE_LOGS_ONLY"></a><a id="csbackup_type_logs_only"></a><dl>
<dt><b>CSBACKUP_TYPE_LOGS_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Backup the log files only.

</td>
</tr>
</table>

### -param phbc [out]

A pointer to a Certificate Services backup context handle (<b>HCSBC</b>).

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success, and *<i>phbc</i> will be set to an <b>HCSBC</b> which can be used by other Certificate Services backup APIs.

## -remarks

Before a Certificate Services backup can occur, it is necessary to create an <b>HCSBC</b> by means of <b>CertSrvBackupPrepare</b>. The resulting <b>HCSBC</b> is a necessary parameter of Certificate Services backup functions which can be used to list, open, read, and close files, as well as truncate the log files.

<div class="alert"><b>Note</b>  When the backup session is completed, it is necessary to call 
<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupend">CertSrvBackupEnd</a> to release the <b>HCSBC</b> which resulted from the call to <b>CertSrvBackupPrepare</b>.</div>
<div> </div>
This function's name in Certadm.dll is <b>CertSrvBackupPrepareW</b>. You must use this form of the name when calling <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVBACKUPPREPAREW</b> in the Certbcli.h header file.

To execute this call, you must have the backup <a href="/windows/desktop/SecGloss/p-gly">privilege</a>. For details, see 
<a href="/windows/desktop/SecCrypto/setting-the-backup-and-restore-privileges">Setting the Backup and Restore Privileges</a>.


#### Examples


```cpp
WCHAR *    wszServer = L"MyCertServerMachine";
FNCERTSRVBACKUPPREPAREW* pfnBackupPrepare;
char * szBackPrepFunc = "CertSrvBackupPrepareW";
HINSTANCE  hInst=0;
HCSBC      hCSBC=NULL;
HRESULT    hr=0;

// Load the DLL.
hInst = LoadLibrary(L"Certadm.dll");
if ( NULL == hInst )
{
    printf("Failed LoadLibrary, error=%d\n",
            GetLastError() );
    exit(1); // Or other appropriate error action.
}
// Get the address for the desired function.
pfnBackupPrepare = (FNCERTSRVBACKUPPREPAREW*)GetProcAddress( hInst,
                                        szBackPrepFunc );
if ( NULL == pfnBackupPrepare )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szBackPrepFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// Prepare CertServ for backup.
hr = pfnBackupPrepare(wszServer,
                      0,
                      CSBACKUP_TYPE_FULL,
                      &hCSBC);
if (FAILED(hr))
{
    printf("Failed pfnBackupPrepare call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}

// Use the HCSBC for backup operations.
// ...

// When done processing, release the HCSBC context
// by calling CertSrvBackupEnd (not shown here).
// ...


// Done processing, free the DLL.
if (hInst)
    FreeLibrary(hInst);

```

## -see-also

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupend">CertSrvBackupEnd</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>