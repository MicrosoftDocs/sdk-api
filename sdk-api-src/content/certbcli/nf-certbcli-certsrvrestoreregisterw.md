---
UID: NF:certbcli.CertSrvRestoreRegisterW
title: CertSrvRestoreRegisterW function (certbcli.h)
description: Registers a Certificate Services restore. (CertSrvRestoreRegisterW)
helpviewer_keywords: ["CertSrvRestoreRegister","CertSrvRestoreRegister function [Security]","CertSrvRestoreRegisterW","FNCERTSRVRESTOREREGISTERW","FNCERTSRVRESTOREREGISTERW function [Security]","_certsrv_certsrvrestoreregister","certbcli/CertSrvRestoreRegister","certbcli/CertSrvRestoreRegisterW","certbcli/FNCERTSRVRESTOREREGISTERW","security.certsrvrestoreregister"]
old-location: security\certsrvrestoreregister.htm
tech.root: security
ms.assetid: 4549ba26-d52c-4779-b27d-126cef6ef15d
ms.date: 12/05/2018
ms.keywords: CertSrvRestoreRegister, CertSrvRestoreRegister function [Security], CertSrvRestoreRegisterW, FNCERTSRVRESTOREREGISTERW, FNCERTSRVRESTOREREGISTERW function [Security], _certsrv_certsrvrestoreregister, certbcli/CertSrvRestoreRegister, certbcli/CertSrvRestoreRegisterW, certbcli/FNCERTSRVRESTOREREGISTERW, security.certsrvrestoreregister
req.header: certbcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertSrvRestoreRegisterW (Unicode)
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
 - CertSrvRestoreRegisterW
 - certbcli/CertSrvRestoreRegisterW
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
 - CertSrvRestoreRegister
 - CertSrvRestoreRegisterW
---

# CertSrvRestoreRegisterW function


## -description

The <b>CertSrvRestoreRegister</b> function registers a Certificate Services restore.

## -parameters

### -param hbc [in]

A handle to the Certificate Services restore context. This handle is obtained by calling 
the <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestorepreparew">CertSrvRestorePrepare</a> function.

### -param pwszCheckPointFilePath [in]

A pointer to a null-terminated Unicode string that contains the restore path for the check point file. Pass <b>NULL</b> for this parameter if it is not needed.

### -param pwszLogPath [in]

A pointer to a null-terminated Unicode string that contains the current log file directory. Pass <b>NULL</b> for this parameter if it is not needed.

### -param rgrstmap [in]

An array of <b>CSEDB_RSTMAP</b> structures that contains the restore map. If you are performing a full database restoration, this parameter specifies the name of the backup database, as well as a new name for the database after it is restored. The backup database name is referenced by the <b>pwszDatabaseName</b> member, and the new database name is referenced by the <b>pwszNewDatabaseName</b> member. If the intent is to maintain the same name for both the backup database and the restored database, set both the <b>pwszNewDatabaseName</b> and the <b>pwszDatabaseName</b> members to the same name. The backup database name is constructed from the path returned by the backup client's call to 
the <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw">CertSrvRestoreGetDatabaseLocations</a> function. <b>CertSrvRestoreGetDatabaseLocations</b> would have been called during a full backup, and the backup client would have saved the returned path.

If you are performing an incremental restoration, pass <b>NULL</b> for this parameter.

### -param crstmap [in]

The number of elements in the <i>rgrstmap</i> array. Pass zero for this parameter if you are performing an incremental restoration.

### -param pwszBackupLogPath [in]

A pointer to a null-terminated Unicode string that contains the path for the backup log directory. Pass <b>NULL</b> for this parameter if it is not needed.

### -param genLow [in]

The lowest log number that was restored in this restore session. Log files are in the form of edbXXXXX.log, where XXXXX is a five hexadecimal digit value. For example, edb00001.log is the first log file created by the internal database. For purposes of this function, a value of one in <i>genLow</i> corresponds to the log file edb00001.log.

### -param genHigh [in]

The highest log number that was restored in this restore session.

## -returns

The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates success.

## -remarks

Use this function to register a restore operation. All subsequent restore operations will be interlocked. The restore target will be prevented from starting (or successfully executing another call to <b>CertSrvRestoreRegister</b>) until 
<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoreregistercomplete">CertSrvRestoreRegisterComplete</a> is called.

When restoring more than one incremental backup, the order in which the incremental backups are registered does not matter. However, the full database backup must be registered before registering the incremental backups.

This function requires that the calling account be  a local administrator. If this is not practical, use the <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoreregisterthroughfile">CertSrvRestoreRegisterThroughFile</a> function instead. The <b>CertSrvRestoreRegisterThroughFile</b> function only requires that the calling account have the restore privilege.


#### Examples


```cpp
// szMyDBName is the returned path from the backup client's
// call to CertSrvRestoreGetDatabaseLocations. This value would
// have been saved during a full backup operation.
CSEDB_RSTMAP rgrstmap[1] = 
{ 
    szMyDBName, // database name
    szMyDBName  // new name same as old
};

HRESULT hr = 0;

// Register a restore operation.
// hsb is an HCSBC created previously by CertSrvRestorePrepare.
hr = CertSrvRestoreRegister( 
    hsb,
    NULL,
    szMyRestoreLogPath, // defined elsewhere
    rgrstmap,
    1,
    szMyBackupLogPath, // defined elsewhere
    1,    // edb00001.log
    0x1a  // edb0001a.log
    );

if (S_OK != hr)
{
    printf("Failed CertSrvRestoreRegister - %x\n", hr);
    exit(1); // Or other appropriate error action.
}

// Continue processing.
// When done, call CertSrvRestoreRegisterComplete (not shown).
// ...
```

## -see-also

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoreregistercomplete">CertSrvRestoreRegisterComplete</a>



<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoreregisterthroughfile">CertSrvRestoreRegisterThroughFile</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>
