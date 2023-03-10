---
UID: NL:vsbackup.IVssExamineWriterMetadata
title: IVssExamineWriterMetadata (vsbackup.h)
description: The IVssExamineWriterMetadata interface is a C++ (not COM) interface that allows a requester to examine the metadata of a specific writer instance.
helpviewer_keywords: ["IVssExamineWriterMetadata","IVssExamineWriterMetadata interface [VSS]","IVssExamineWriterMetadata interface [VSS]","described","_win32_ivssexaminewritermetadata","base.ivssexaminewritermetadata","vsbackup/IVssExamineWriterMetadata"]
old-location: base\ivssexaminewritermetadata.htm
tech.root: base
ms.assetid: b3aa04d9-7299-4e3a-b092-d07f2de6eefe
ms.date: 12/05/2018
ms.keywords: IVssExamineWriterMetadata, IVssExamineWriterMetadata interface [VSS], IVssExamineWriterMetadata interface [VSS],described, _win32_ivssexaminewritermetadata, base.ivssexaminewritermetadata, vsbackup/IVssExamineWriterMetadata
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
 - IVssExamineWriterMetadata
 - vsbackup/IVssExamineWriterMetadata
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
 - IVssExamineWriterMetadata
---

# IVssExamineWriterMetadata class


## -description

The 
<b>IVssExamineWriterMetadata</b> interface is a C++ (not COM) interface that allows a requester to examine the metadata of a specific writer instance. This metadata may come from a currently executing (live) writer, or it may have been stored as an XML document.

An 
<b>IVssExamineWriterMetadata</b> interface to a live writer's metadata is obtained by a call to 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata">IVssBackupComponents::GetWriterMetadata</a>.

Metadata obtained from a stored XML document can be examined by an instance of 
<b>IVssExamineWriterMetadata</b> obtained by a call to 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-createvssexaminewritermetadata">CreateVssExamineWriterMetadata</a>.

## -inheritance

The <b>IVssExamineWriterMetadata</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssExamineWriterMetadata</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>
