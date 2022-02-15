---
UID: NE:wmcodecdsp.TOC_POS_TYPE
title: TOC_POS_TYPE (wmcodecdsp.h)
description: The TOC_POS_TYPE enumeration contains members that specify the position type of a table of contents.
helpviewer_keywords: ["TOC_POS_INHEADER","TOC_POS_TOPLEVELOBJECT","TOC_POS_TYPE","TOC_POS_TYPE enumeration [Media Foundation]","codecapi.toc_pos_type","mf.toc_pos_type","wmcodecdsp/TOC_POS_INHEADER","wmcodecdsp/TOC_POS_TOPLEVELOBJECT","wmcodecdsp/TOC_POS_TYPE"]
old-location: mf\toc_pos_type.htm
tech.root: mf
ms.assetid: 799059b5-9949-48af-8c54-4cb4975f8249
ms.date: 12/05/2018
ms.keywords: TOC_POS_INHEADER, TOC_POS_TOPLEVELOBJECT, TOC_POS_TYPE, TOC_POS_TYPE enumeration [Media Foundation], codecapi.toc_pos_type, mf.toc_pos_type, wmcodecdsp/TOC_POS_INHEADER, wmcodecdsp/TOC_POS_TOPLEVELOBJECT, wmcodecdsp/TOC_POS_TYPE
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TOC_POS_TYPE
 - wmcodecdsp/TOC_POS_TYPE
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
 - TOC_POS_TYPE
---

# TOC_POS_TYPE enumeration


## -description

The <b>TOC_POS_TYPE</b> enumeration contains members that specify the <a href="/windows/desktop/medfound/the-position-type-of-a-table-of-contents">position type</a> of a table of contents.

## -enum-fields

### -field TOC_POS_INHEADER:0

Specifies that the table of contents is stored in the header of the media file.

### -field TOC_POS_TOPLEVELOBJECT

Specifies that the table of contents is stored in the body of the media file as a top level object.

## -remarks

Currently, only <b>TOC_POS_TOPLEVELOBJECT</b> is supported.

## -see-also

<a href="/windows/desktop/medfound/toc-parser-enumerations">Table of Contents Parser Enumerations</a>



<a href="/windows/desktop/medfound/the-position-type-of-a-table-of-contents">The Position Type of a Table of Contents</a>
