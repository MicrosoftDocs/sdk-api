---
UID: NL:vsbackup.IVssBackupComponents
title: IVssBackupComponents (vsbackup.h)
description: The IVssBackupComponents interface is used by a requester to poll writers about file status and to run backup/restore operations.
helpviewer_keywords: ["IVssBackupComponents","IVssBackupComponents interface [VSS]","IVssBackupComponents interface [VSS]","described","_win32_ivssbackupcomponents","base.ivssbackupcomponents","vsbackup/IVssBackupComponents"]
old-location: base\ivssbackupcomponents.htm
tech.root: base
ms.assetid: fe1220c7-11e5-4872-b7a9-61558f7c75c0
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents, IVssBackupComponents interface [VSS], IVssBackupComponents interface [VSS],described, _win32_ivssbackupcomponents, base.ivssbackupcomponents, vsbackup/IVssBackupComponents
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
 - IVssBackupComponents
 - vsbackup/IVssBackupComponents
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
 - IVssBackupComponents
---

# IVssBackupComponents class


## -description

The <b>IVssBackupComponents</b> interface is used by a 
    requester to poll writers about file status and to run backup/restore operations.

Applications obtain an instance of the 
    <b>IVssBackupComponents</b> interface by calling 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-createvssbackupcomponents">CreateVssBackupComponents</a>.

An <b>IVssBackupComponents</b> object can be used for 
    only a single backup, restore, or <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">Query</a> operation.

After the backup, restore, or <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">Query</a> operation has either successfully finished or been explicitly terminated, a requester must 
    release the <b>IVssBackupComponents</b> object by calling 
    <b>IVssBackupComponents::Release</b>. An 
    <b>IVssBackupComponents</b> object must not be reused. For example, you cannot perform a backup or restore operation with the same <b>IVssBackupComponents</b> object that you have already used for a <b>Query</b> operation.

## -inheritance

The <b>IVssBackupComponents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssBackupComponents</b> also has these types of members:

