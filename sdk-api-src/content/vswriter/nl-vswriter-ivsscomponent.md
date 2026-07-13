---
UID: NL:vswriter.IVssComponent
title: IVssComponent (vswriter.h)
description: The IVssComponent interface is a C++ (not COM) interface containing methods for examining and modifying information about components contained in a requester's Backup Components Document.
helpviewer_keywords: ["IVssComponent","IVssComponent interface [VSS]","IVssComponent interface [VSS]","described","_win32_ivsscomponent","base.ivsscomponent","vswriter/IVssComponent"]
old-location: base\ivsscomponent.htm
tech.root: base
ms.assetid: c686a424-b0b9-4efc-8dc6-b92193de2a5d
ms.date: 12/05/2018
ms.keywords: IVssComponent, IVssComponent interface [VSS], IVssComponent interface [VSS],described, _win32_ivsscomponent, base.ivsscomponent, vswriter/IVssComponent
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
 - IVssComponent
 - vswriter/IVssComponent
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
 - IVssComponent
---

# IVssComponent class


## -description

The <b>IVssComponent</b> interface is a C++ (not COM) interface 
    containing methods for examining and modifying information about components contained in a requester's Backup 
    Components Document.

<b>IVssComponent</b> objects can be obtained only for those 
    components that have been explicitly added to the Backup Components Document during a backup operation by the 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a> 
    method.

Information about components explicitly added during a restore operation using 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent"> IVssBackupComponents::AddRestoreSubcomponent</a> 
    are not available through the <b>IVssComponent</b> interface.

Some information common to both components and implicitly selected subcomponents available through 
    <b>IVssComponent</b> objects includes the following:
<ul>
<li>Backup time stamp</li>
<li>Pre-/post-restore Failure Messages</li>
<li>Restore metadata</li>
<li>Restore target</li>
</ul>Some information in the <b>IVssComponent</b> object is on a 
    per-file basis and can refer to files managed either by explicitly selected components or by implicitly selected 
    subcomponents:
<ul>
<li>Alternate location mappings</li>
<li>Partial files</li>
<li>Directed target</li>
</ul>Other information is not included in the Backup Components Document and can be inferred using the 
    <b>IVssComponent</b> object in conjunction with the appropriate 
    Writer Metadata Documents based on a writer's component hierarchy expressed in the logical paths (see 
    <a href="/windows/desktop/VSS/working-with-selectability-and-logical-paths">Working with Selectability and 
    Logical Paths</a>).

The interface can be used by either a writer or a requester, although certain methods are supported only for 
    writers. In this way, a writer can request changes in a backup or restore operation, such as adding a new target, 
    or learn of requester actions, such as the use of an alternate location.

The following methods return an <b>IVssComponent</b> 
    interface:
<ul>
<li>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswritercomponents-getcomponent">IVssWriterComponents::GetComponent</a>
</li>
<li>
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswritercomponentsext">IVssWriterComponentsExt::GetComponent</a>
</li>
</ul>

## -inheritance

The <b>IVssComponent</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssComponent</b> also has these types of members:

