---
UID: NS:wmcodecdsp._TOC_DESCRIPTOR
title: TOC_DESCRIPTOR (wmcodecdsp.h)
description: The TOC_DESCRIPTOR structure holds descriptive information for a table of contents.
helpviewer_keywords: ["TOC_DESCRIPTOR","TOC_DESCRIPTOR structure [Media Foundation]","codecapi.toc_descriptor","mf.toc_descriptor","wmcodecdsp/TOC_DESCRIPTOR"]
old-location: mf\toc_descriptor.htm
tech.root: mf
ms.assetid: a79f75c5-be98-4120-85be-71bedbcc0ea2
ms.date: 12/05/2018
ms.keywords: TOC_DESCRIPTOR, TOC_DESCRIPTOR structure [Media Foundation], codecapi.toc_descriptor, mf.toc_descriptor, wmcodecdsp/TOC_DESCRIPTOR
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TOC_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOC_DESCRIPTOR
 - wmcodecdsp/_TOC_DESCRIPTOR
 - TOC_DESCRIPTOR
 - wmcodecdsp/TOC_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcodecdsp.h
api_name:
 - TOC_DESCRIPTOR
---

# TOC_DESCRIPTOR structure


## -description

The <b>TOC_DESCRIPTOR</b> structure holds descriptive information for a table of contents.

## -struct-fields

### -field guidID

A globally unique identifier (<b>GUID</b>) that identifies an individual table of contents. This identifier has meaning only to the you, the developer. TOC Parser does not inspect or interpret this identifier.

### -field wStreamNumber

Not used.

### -field guidType

A globally unique identifier (<b>GUID</b>) that identifies a table of contents as belonging to a particular type. This identifier has meaning only to you, the developer. TOC Parser does not inspect or interpret this identifier. See Remarks.

### -field wLanguageIndex

An integer that identifies the language of a table of contents. This index has meaning only to you, the developer. TOC Parser does not inspect or interpret this index.

## -remarks

You might want to design several different type of tables of contents. In that case, you can distinguish between types by creating a <b>GUID</b> that represents each type. You can identify a table of contents as a particular type by setting the <b>guidType</b> member of a <b>TOC_DESCRIPTOR</b> structure and then passing the structure to <a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-setdescriptor">IToc::SetDescriptor</a>.

## -see-also

<a href="/windows/desktop/medfound/toc-parser-structures">Table of Contents Parser Structures</a>