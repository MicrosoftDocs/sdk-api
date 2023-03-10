---
UID: NF:vswriter.CVssWriter.GetBackupType
title: CVssWriter::GetBackupType (vswriter.h)
description: The GetBackupType method indicates the type of backup to be performed.
helpviewer_keywords: ["CVssWriter interface [VSS]","GetBackupType method","CVssWriter.GetBackupType","CVssWriter::GetBackupType","GetBackupType","GetBackupType method [VSS]","GetBackupType method [VSS]","CVssWriter interface","_win32_cvsswriter_getbackuptype","base.cvsswriter_getbackuptype","vswriter/CVssWriter::GetBackupType"]
old-location: base\cvsswriter_getbackuptype.htm
tech.root: base
ms.assetid: b8f78552-27b5-4d64-9d35-baf1c636b526
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],GetBackupType method, CVssWriter.GetBackupType, CVssWriter::GetBackupType, GetBackupType, GetBackupType method [VSS], GetBackupType method [VSS],CVssWriter interface, _win32_cvsswriter_getbackuptype, base.cvsswriter_getbackuptype, vswriter/CVssWriter::GetBackupType
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CVssWriter::GetBackupType
 - vswriter/CVssWriter::GetBackupType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriter.GetBackupType
---

# CVssWriter::GetBackupType


## -description

The 
<b>GetBackupType</b> method indicates the type of backup to be performed.

<b>GetBackupType</b> is a protected method implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.



## -returns

This method returns the backup type as a 
<a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a> enumeration value. See 
<b>VSS_BACKUP_TYPE</b> for a description of these values.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupcomplete">CVssWriter::OnBackupComplete</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore">CVssWriter::OnPostRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a>
