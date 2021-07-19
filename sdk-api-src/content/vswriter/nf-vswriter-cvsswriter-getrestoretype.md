---
UID: NF:vswriter.CVssWriter.GetRestoreType
title: CVssWriter::GetRestoreType (vswriter.h)
description: The GetRestoreType method returns the type of restore a writer is participating in.
helpviewer_keywords: ["CVssWriter interface [VSS]","GetRestoreType method","CVssWriter.GetRestoreType","CVssWriter::GetRestoreType","GetRestoreType","GetRestoreType method [VSS]","GetRestoreType method [VSS]","CVssWriter interface","_win32_cvsswriter_getrestoretype","base.cvsswriter_getrestoretype","vswriter/CVssWriter::GetRestoreType"]
old-location: base\cvsswriter_getrestoretype.htm
tech.root: base
ms.assetid: 438298ee-ab8b-4604-9d43-5acefd7cabd5
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],GetRestoreType method, CVssWriter.GetRestoreType, CVssWriter::GetRestoreType, GetRestoreType, GetRestoreType method [VSS], GetRestoreType method [VSS],CVssWriter interface, _win32_cvsswriter_getrestoretype, base.cvsswriter_getrestoretype, vswriter/CVssWriter::GetRestoreType
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - CVssWriter::GetRestoreType
 - vswriter/CVssWriter::GetRestoreType
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
 - CVssWriter.GetRestoreType
---

# CVssWriter::GetRestoreType


## -description

The 
<b>GetRestoreType</b> method returns the type of restore a writer is participating in.

<b>GetRestoreType</b> is a protected method implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.



## -returns

This method returns the type of restore operation a writer is participating in, in terms of values of the 
<a href="/windows/desktop/api/vss/ne-vss-vss_restore_type">VSS_RESTORE_TYPE</a> enumeration.

If 
<b>GetRestoreType</b> is called during a backup operation, the return value is undefined.

## -remarks

This method should be called only during restore operations.

The default restore type is VSS_RTYPE_UNDEFINED. However, writers should treat this restore type as if it were VSS_RTYPE_BY_COPY.

A requester can set the restore type by calling the 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrestorestate">IVssBackupComponents::SetRestoreState</a> method.

A requester can call <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrestorestate">IVssBackupComponents::SetRestoreState</a> anytime prior to its generation of a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> event with the 
<b>IVssBackupComponents::PreRestore</b> method. Therefore, to obtain the correct restore type, a writer should not call 
<b>GetRestoreType</b> prior to handling the 
<b>PreRestore</b> event in 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrestorestate">IVssBackupComponents::SetRestoreState</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_restore_type">VSS_RESTORE_TYPE</a>
