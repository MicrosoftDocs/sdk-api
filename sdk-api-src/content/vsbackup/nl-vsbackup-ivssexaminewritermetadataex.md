---
UID: NL:vsbackup.IVssExamineWriterMetadataEx
title: IVssExamineWriterMetadataEx (vsbackup.h)
description: Provides a method to retrieve the writer instance name and other basic information for a specific writer instance.
helpviewer_keywords: ["IVssExamineWriterMetadataEx","IVssExamineWriterMetadataEx interface [VSS]","IVssExamineWriterMetadataEx interface [VSS]","described","base.ivssexaminewritermetadataex","vsbackup/IVssExamineWriterMetadataEx"]
old-location: base\ivssexaminewritermetadataex.htm
tech.root: base
ms.assetid: 363c987c-7d6c-4efe-988a-1b288f9b4d3c
ms.date: 12/05/2018
ms.keywords: IVssExamineWriterMetadataEx, IVssExamineWriterMetadataEx interface [VSS], IVssExamineWriterMetadataEx interface [VSS],described, base.ivssexaminewritermetadataex, vsbackup/IVssExamineWriterMetadataEx
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssExamineWriterMetadataEx
 - vsbackup/IVssExamineWriterMetadataEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsBackup.h
api_name:
 - IVssExamineWriterMetadataEx
---

# IVssExamineWriterMetadataEx class


## -description

The <b>IVssExamineWriterMetadataEx</b> interface is a C++ (not COM) interface that provides a method to retrieve the writer instance name and other basic information for a specific writer instance.

To obtain an instance of the <b>IVssExamineWriterMetadataEx</b> 
   interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> interface, passing 
   <b>IID_IVssExamineWriterMetadataEx</b> as the interface identifier (IID) parameter.

## -inheritance

The <b>IVssExamineWriterMetadataEx</b> interface inherits from <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>. <b>IVssExamineWriterMetadataEx</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>
