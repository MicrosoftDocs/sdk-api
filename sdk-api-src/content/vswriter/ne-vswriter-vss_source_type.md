---
UID: NE:vswriter.VSS_SOURCE_TYPE
title: VSS_SOURCE_TYPE (vswriter.h)
description: Specifies the type of data that a writer manages.
helpviewer_keywords: ["VSS_SOURCE_TYPE","VSS_SOURCE_TYPE enumeration [VSS]","VSS_ST_NONTRANSACTEDDB","VSS_ST_OTHER","VSS_ST_TRANSACTEDDB","VSS_ST_UNDEFINED","_win32_vss_source_type","base.vss_source_type","enumeration [VSS]","vswriter/VSS_SOURCE_TYPE","vswriter/VSS_ST_NONTRANSACTEDDB","vswriter/VSS_ST_OTHER","vswriter/VSS_ST_TRANSACTEDDB","vswriter/VSS_ST_UNDEFINED"]
old-location: base\vss_source_type.htm
tech.root: base
ms.assetid: cb89c3cc-5a8e-419e-839c-f72a1886eadf
ms.date: 12/05/2018
ms.keywords: VSS_SOURCE_TYPE, VSS_SOURCE_TYPE enumeration [VSS], VSS_ST_NONTRANSACTEDDB, VSS_ST_OTHER, VSS_ST_TRANSACTEDDB, VSS_ST_UNDEFINED, _win32_vss_source_type, base.vss_source_type, enumeration [VSS], vswriter/VSS_SOURCE_TYPE, vswriter/VSS_ST_NONTRANSACTEDDB, vswriter/VSS_ST_OTHER, vswriter/VSS_ST_TRANSACTEDDB, vswriter/VSS_ST_UNDEFINED
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
req.typenames: VSS_SOURCE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VSS_SOURCE_TYPE
 - vswriter/VSS_SOURCE_TYPE
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
 - VSS_SOURCE_TYPE
---

# VSS_SOURCE_TYPE enumeration


## -description

The <b>VSS_SOURCE_TYPE</b> enumeration specifies the 
    type of data that a writer manages.

## -enum-fields

### -field VSS_ST_UNDEFINED:0

The source of the data is not known. 
      

This indicates a writer error, and the requester should report it.

### -field VSS_ST_TRANSACTEDDB

The source of the data is a database that supports transactions, such as Microsoft SQL Server.

### -field VSS_ST_NONTRANSACTEDDB

The source of the data is a database that does not support transactions.

### -field VSS_ST_OTHER

Unclassified source type—data will be in a file group. 
      

This is the default source type.

## -remarks

The source type of the data that a writer manages is specified when it initializes its cooperation with the 
    shadow copy mechanism through a call to 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>.

Information about the source type of the data that a writer manages can be retrieved through its metadata 
    using 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getidentity">IVssExamineWriterMetadata::GetIdentity</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getidentity">IVssExamineWriterMetadata::GetIdentity</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_object_type">VSS_OBJECT_TYPE</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_usage_type">VSS_USAGE_TYPE</a>
