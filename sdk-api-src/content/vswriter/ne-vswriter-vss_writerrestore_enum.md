---
UID: NE:vswriter.VSS_WRITERRESTORE_ENUM
title: VSS_WRITERRESTORE_ENUM (vswriter.h)
description: Indicate to a requester the conditions under which it will handle events generated during a restore operation.
helpviewer_keywords: ["VSS_WRE_ALWAYS","VSS_WRE_IF_REPLACE_FAILS","VSS_WRE_NEVER","VSS_WRE_UNDEFINED","VSS_WRITERRESTORE_ENUM","VSS_WRITERRESTORE_ENUM enumeration [VSS]","_win32_vss_writerrestore_enum","base.vss_writerrestore_enum","enumeration [VSS]","vswriter/VSS_WRE_ALWAYS","vswriter/VSS_WRE_IF_REPLACE_FAILS","vswriter/VSS_WRE_NEVER","vswriter/VSS_WRE_UNDEFINED","vswriter/VSS_WRITERRESTORE_ENUM"]
old-location: base\vss_writerrestore_enum.htm
tech.root: base
ms.assetid: a3e45d52-4d9a-4bdf-a8e5-622939be6f2c
ms.date: 12/05/2018
ms.keywords: VSS_WRE_ALWAYS, VSS_WRE_IF_REPLACE_FAILS, VSS_WRE_NEVER, VSS_WRE_UNDEFINED, VSS_WRITERRESTORE_ENUM, VSS_WRITERRESTORE_ENUM enumeration [VSS], _win32_vss_writerrestore_enum, base.vss_writerrestore_enum, enumeration [VSS], vswriter/VSS_WRE_ALWAYS, vswriter/VSS_WRE_IF_REPLACE_FAILS, vswriter/VSS_WRE_NEVER, vswriter/VSS_WRE_UNDEFINED, vswriter/VSS_WRITERRESTORE_ENUM
req.header: vswriter.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VSS_WRITERRESTORE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VSS_WRITERRESTORE_ENUM
 - vswriter/VSS_WRITERRESTORE_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsWriter.h
api_name:
 - VSS_WRITERRESTORE_ENUM
---

# VSS_WRITERRESTORE_ENUM enumeration


## -description

The <b>VSS_WRITERRESTORE_ENUM</b> enumeration is used by 
    a writer to indicate to a requester the conditions under which it will handle events generated during a 
    restore operation.

## -enum-fields

### -field VSS_WRE_UNDEFINED:0

It is not known whether the writer will perform special operations during the restore operation. 
      

This state indicates a writer error.

### -field VSS_WRE_NEVER

The writer does not require restore events.

### -field VSS_WRE_IF_REPLACE_FAILS

Indicates that the writer always expects to handle a 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> 
      (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CvssWriter::OnPreRestore</a>) event, but expects 
      to handle a <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">PostRestore</a> event 
      (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore">CvssWriter::OnPostRestore</a>) only if a restore 
      fails when implementing either a <b>VSS_RME_RESTORE_IF_NOT_THERE</b> or 
      <b>VSS_RME_RESTORE_IF_CAN_REPLACE</b> restore method 
      (<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_restoremethod_enum">VSS_RESTOREMETHOD_ENUM</a>).

### -field VSS_WRE_ALWAYS

The writer always performs special operations during the restore operation.

## -remarks

A writer passes a value of 
    <b>VSS_WRITERRESTORE_ENUM</b> to 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod">IVssCreateWriterMetadata::SetRestoreMethod</a> 
    to indicate through its metadata how it interacts with requesters during a restore operation.

A requester retrieves information about a writer's participation by calling 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod">IVssExamineWriterMetadata::GetRestoreMethod</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod">IVssCreateWriterMetadata::SetRestoreMethod</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod">IVssExamineWriterMetadata::GetRestoreMethod</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_restoremethod_enum">VSS_RESTOREMETHOD_ENUM</a>
