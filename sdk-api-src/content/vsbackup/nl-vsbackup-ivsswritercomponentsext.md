---
UID: NL:vsbackup.IVssWriterComponentsExt
title: IVssWriterComponentsExt (vsbackup.h)
description: The IVssWriterComponentsExt interface is a C++ (not COM) interface used by requesters to access and modify the components of a writer involved in a backup.
helpviewer_keywords: ["IVssWriterComponentsExt","IVssWriterComponentsExt interface [VSS]","IVssWriterComponentsExt interface [VSS]","described","_win32_ivsswritercomponentsext","base.ivsswritercomponentsext","vsbackup/IVssWriterComponentsExt"]
old-location: base\ivsswritercomponentsext.htm
tech.root: base
ms.assetid: 29772c1f-1cc4-4ee7-8e1d-f1a6cbebf470
ms.date: 12/05/2018
ms.keywords: IVssWriterComponentsExt, IVssWriterComponentsExt interface [VSS], IVssWriterComponentsExt interface [VSS],described, _win32_ivsswritercomponentsext, base.ivsswritercomponentsext, vsbackup/IVssWriterComponentsExt
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
 - IVssWriterComponentsExt
 - vsbackup/IVssWriterComponentsExt
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
 - IVssWriterComponentsExt
---

# IVssWriterComponentsExt class


## -description

The 
<b>IVssWriterComponentsExt</b> interface is a C++ (not COM) interface used by requesters to access and modify the components of a writer involved in a backup.

<b>IVssWriterComponentsExt</b> is returned by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents">IVssBackupComponents::GetWriterComponents</a> and inherits from 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a> and <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>.
<div class="alert"><b>Note</b>  During the restore phase, the requester should call <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswritercomponents-getcomponent">IVssWriterComponentsExt::GetComponent</a> or <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswritercomponents-getcomponentcount">IVssWriterComponentsExt::GetComponentCount</a> only after the call to <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a> has returned, to allow time for the writer to update the Backup Components Document. One example of such an update would be to change the restore target.</div><div> </div>Life cycle management of 
<b>IVssWriterComponentsExt</b> is handled through the inherited <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> methods. Specifically, an application is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release resources held by an 
<b>IVssWriterComponentsExt</b> object.

<b>IVssWriterComponentsExt</b> does not define any methods.