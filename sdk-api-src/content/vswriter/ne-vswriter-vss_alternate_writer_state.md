---
UID: NE:vswriter.VSS_ALTERNATE_WRITER_STATE
title: VSS_ALTERNATE_WRITER_STATE (vswriter.h)
description: Used to indicate whether a given writer has an associated alternate writer.
helpviewer_keywords: ["VSS_ALTERNATE_WRITER_STATE","VSS_ALTERNATE_WRITER_STATE enumeration [VSS]","VSS_AWS_ALTERNATE_WRITER_EXISTS","VSS_AWS_NO_ALTERNATE_WRITER","VSS_AWS_THIS_IS_ALTERNATE_WRITER","VSS_AWS_UNDEFINED","_win32_vss_alternate_writer_state","base.vss_alternate_writer_state","enumeration [VSS]","vswriter/VSS_ALTERNATE_WRITER_STATE","vswriter/VSS_AWS_ALTERNATE_WRITER_EXISTS","vswriter/VSS_AWS_NO_ALTERNATE_WRITER","vswriter/VSS_AWS_THIS_IS_ALTERNATE_WRITER","vswriter/VSS_AWS_UNDEFINED"]
old-location: base\vss_alternate_writer_state.htm
tech.root: base
ms.assetid: 8d41fd9d-6448-4bec-a669-4aa50f37cada
ms.date: 12/05/2018
ms.keywords: VSS_ALTERNATE_WRITER_STATE, VSS_ALTERNATE_WRITER_STATE enumeration [VSS], VSS_AWS_ALTERNATE_WRITER_EXISTS, VSS_AWS_NO_ALTERNATE_WRITER, VSS_AWS_THIS_IS_ALTERNATE_WRITER, VSS_AWS_UNDEFINED, _win32_vss_alternate_writer_state, base.vss_alternate_writer_state, enumeration [VSS], vswriter/VSS_ALTERNATE_WRITER_STATE, vswriter/VSS_AWS_ALTERNATE_WRITER_EXISTS, vswriter/VSS_AWS_NO_ALTERNATE_WRITER, vswriter/VSS_AWS_THIS_IS_ALTERNATE_WRITER, vswriter/VSS_AWS_UNDEFINED
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
req.typenames: VSS_ALTERNATE_WRITER_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VSS_ALTERNATE_WRITER_STATE
 - vswriter/VSS_ALTERNATE_WRITER_STATE
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
 - VSS_ALTERNATE_WRITER_STATE
---

# VSS_ALTERNATE_WRITER_STATE enumeration


## -description

The <b>VSS_ALTERNATE_WRITER_STATE</b> enumeration 
    is used to indicate whether a given writer has an associated alternate writer. The existence 
    of an alternate writer is set during writer initialization by 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>.

Currently, the only supported value for a method taking a 
    <b>VSS_ALTERNATE_WRITER_STATE</b> argument is 
    <b>VSS_AWS_NO_ALTERNATE_WRITER</b>.

## -enum-fields

### -field VSS_AWS_UNDEFINED:0

No information is available as to the existence of an alternate writer. This value indicates an application 
      error. This enumeration value is reserved for future use.

### -field VSS_AWS_NO_ALTERNATE_WRITER

A given writer does not have an alternate writer.

### -field VSS_AWS_ALTERNATE_WRITER_EXISTS

An alternate writer exists. This alternate writer runs when the writer is not available. This enumeration 
      value is reserved for future use.

### -field VSS_AWS_THIS_IS_ALTERNATE_WRITER

The writer in question is an alternate writer. This enumeration value is reserved for future use.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onvssapplicationstartup">CVssWriter::OnVSSApplicationStartup</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_writer_state">VSS_WRITER_STATE</a>
