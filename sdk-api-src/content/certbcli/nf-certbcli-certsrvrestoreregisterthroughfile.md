---
UID: NF:certbcli.CertSrvRestoreRegisterThroughFile
title: CertSrvRestoreRegisterThroughFile function (certbcli.h)
description: Registers a Certificate Services restore. (CertSrvRestoreRegisterThroughFile)
helpviewer_keywords: ["CertSrvRestoreRegisterThroughFile","CertSrvRestoreRegisterThroughFile function [Security]","certbcli/CertSrvRestoreRegisterThroughFile","security.certsrvrestoreregisterthroughfile"]
old-location: security\certsrvrestoreregisterthroughfile.htm
tech.root: security
ms.assetid: 6b929983-9905-48c1-96f3-01d8b39878be
ms.date: 12/05/2018
ms.keywords: CertSrvRestoreRegisterThroughFile, CertSrvRestoreRegisterThroughFile function [Security], certbcli/CertSrvRestoreRegisterThroughFile, security.certsrvrestoreregisterthroughfile
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertSrvRestoreRegisterThroughFile
 - certbcli/CertSrvRestoreRegisterThroughFile
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
 - CertSrvRestoreRegisterThroughFile
---

# CertSrvRestoreRegisterThroughFile function


## -description

The <b>CertSrvRestoreRegisterThroughFile</b> function registers a Certificate Services restore.

## -parameters

### -param hbc [in]

A handle to the Certificate Services restore context. This handle is obtained by calling 
the <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestorepreparew">CertSrvRestorePrepare</a> function.

### -param pwszCheckPointFilePath [in, optional]

A pointer to a null-terminated Unicode string that contains the restore path for the check point file. Pass <b>NULL</b> for this parameter if it is not needed.

### -param pwszLogPath [in, optional]

A pointer to a null-terminated Unicode string that contains the current log file directory. Pass <b>NULL</b> for this parameter if it is not needed.

### -param rgrstmap [in, optional]

An array of <b>CSEDB_RSTMAP</b> structures that contains the restore map. If you are performing a full database restoration, this parameter specifies the name of the backup database, as well as a new name for the database after it is restored. The backup database name is referenced by the <b>pwszDatabaseName</b> member, and the new database name is referenced by the <b>pwszNewDatabaseName</b> member. If the intent is to maintain the same name for both the backup database and the restored database, set both the <b>pwszNewDatabaseName</b> and the <b>pwszDatabaseName</b> members to the same name. The backup database name is constructed from the path returned by the backup client's call to 
the <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw">CertSrvRestoreGetDatabaseLocations</a> function. <b>CertSrvRestoreGetDatabaseLocations</b> would have been called during a full backup, and the backup client would have saved the returned path.

If you are performing an incremental restoration, set this parameter to <b>NULL</b>.

### -param crstmap [in]

The number of elements in the <i>rgrstmap</i> array. Set this value to one if a you are performing a full restoration, or zero if you are performing an incremental restoration.

### -param pwszBackupLogPath [in, optional]

A pointer to a null-terminated Unicode string that contains the path for the backup log directory. Pass <b>NULL</b> for this parameter if it is not needed.

### -param genLow [in]

The lowest log number that was restored in this restore session. Log files are in the form of edbXXXXX.log, where XXXXX is a five hexadecimal digit value. For example, edb00001.log is the first log file created by the internal database. For purposes of this function, a value of one in <i>genLow</i> corresponds to the log file edb00001.log.

### -param genHigh [in]

The highest log number that was restored in this restore session.

## -returns

The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates success.

## -remarks

This function is identical to the <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoreregisterw">CertSrvRestoreRegister</a> function except that <b>CertSrvRestoreRegister</b> requires the calling account to be a local administrator. The <b>CertSrvRestoreRegisterThroughFile</b> function only requires that the calling account have the restore privilege.

## -see-also

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoreregisterw">CertSrvRestoreRegister</a>



<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoreregistercomplete">CertSrvRestoreRegisterComplete</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>
