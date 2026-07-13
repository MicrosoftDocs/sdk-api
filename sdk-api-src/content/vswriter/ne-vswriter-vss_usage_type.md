---
UID: NE:vswriter.VSS_USAGE_TYPE
title: VSS_USAGE_TYPE (vswriter.h)
description: Specifies how the host system uses the data managed by a writer involved in a VSS operation.
helpviewer_keywords: ["VSS_USAGE_TYPE","VSS_USAGE_TYPE enumeration [VSS]","VSS_UT_BOOTABLESYSTEMSTATE","VSS_UT_OTHER","VSS_UT_SYSTEMSERVICE","VSS_UT_UNDEFINED","VSS_UT_USERDATA","_win32_vss_usage_type","base.vss_usage_type","enumeration [VSS]","vswriter/VSS_USAGE_TYPE","vswriter/VSS_UT_BOOTABLESYSTEMSTATE","vswriter/VSS_UT_OTHER","vswriter/VSS_UT_SYSTEMSERVICE","vswriter/VSS_UT_UNDEFINED","vswriter/VSS_UT_USERDATA"]
old-location: base\vss_usage_type.htm
tech.root: base
ms.assetid: 31997417-d993-4f28-b108-ce1dd8239650
ms.date: 12/05/2018
ms.keywords: VSS_USAGE_TYPE, VSS_USAGE_TYPE enumeration [VSS], VSS_UT_BOOTABLESYSTEMSTATE, VSS_UT_OTHER, VSS_UT_SYSTEMSERVICE, VSS_UT_UNDEFINED, VSS_UT_USERDATA, _win32_vss_usage_type, base.vss_usage_type, enumeration [VSS], vswriter/VSS_USAGE_TYPE, vswriter/VSS_UT_BOOTABLESYSTEMSTATE, vswriter/VSS_UT_OTHER, vswriter/VSS_UT_SYSTEMSERVICE, vswriter/VSS_UT_UNDEFINED, vswriter/VSS_UT_USERDATA
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
req.typenames: VSS_USAGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VSS_USAGE_TYPE
 - vswriter/VSS_USAGE_TYPE
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
 - VSS_USAGE_TYPE
---

# VSS_USAGE_TYPE enumeration


## -description

The <b>VSS_USAGE_TYPE</b> enumeration specifies how 
    the host system uses the data managed by a writer involved in a VSS operation.

## -enum-fields

### -field VSS_UT_UNDEFINED:0

The usage type is not known. 
      

This indicates an error on the part of the writer.

### -field VSS_UT_BOOTABLESYSTEMSTATE

The data stored by the writer is part of the bootable system state.

### -field VSS_UT_SYSTEMSERVICE

The writer either stores data used by a system service or is a system service itself.

### -field VSS_UT_USERDATA

The data is user data.

### -field VSS_UT_OTHER

Unclassified data.

## -remarks

The usage type of the data that a writer manages is specified when it initializes its cooperation with the 
    shadow copy mechanism through 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>.

Information about the usage type of the data that a writer manages can be retrieved through its metadata using 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getidentity">IVssExamineWriterMetadata::GetIdentity</a>.

Requester applications that are interested in backing up system state should look for writers with the  <b>VSS_UT_BOOTABLESYSTEMSTATE</b> or  <b>VSS_UT_SYSTEMSERVICE</b> usage type.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getidentity">IVssExamineWriterMetadata::GetIdentity</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_object_type">VSS_OBJECT_TYPE</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_source_type">VSS_SOURCE_TYPE</a>
