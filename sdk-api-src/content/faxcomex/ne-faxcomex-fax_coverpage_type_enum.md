---
UID: NE:faxcomex.FAX_COVERPAGE_TYPE_ENUM
title: FAX_COVERPAGE_TYPE_ENUM (faxcomex.h)
description: The FAX_COVERPAGE_TYPE_ENUM enumeration defines whether a cover page template file is a local computer cover page or a server-based cover page. It can also specify that no file is used.
helpviewer_keywords: ["FAX_COVERPAGE_TYPE_ENUM","FAX_COVERPAGE_TYPE_ENUM enumeration [Fax Service]","_mfax_fax_coverpage_type_enum","fax._mfax_fax_coverpage_type_enum","faxcomex/FAX_COVERPAGE_TYPE_ENUM","faxcomex/fcptLOCAL","faxcomex/fcptNONE","faxcomex/fcptSERVER","fcptLOCAL","fcptNONE","fcptSERVER"]
old-location: fax\_mfax_fax_coverpage_type_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7lm5.htm
ms.date: 12/05/2018
ms.keywords: FAX_COVERPAGE_TYPE_ENUM, FAX_COVERPAGE_TYPE_ENUM enumeration [Fax Service], _mfax_fax_coverpage_type_enum, fax._mfax_fax_coverpage_type_enum, faxcomex/FAX_COVERPAGE_TYPE_ENUM, faxcomex/fcptLOCAL, faxcomex/fcptNONE, faxcomex/fcptSERVER, fcptLOCAL, fcptNONE, fcptSERVER
req.header: faxcomex.h
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
req.typenames: FAX_COVERPAGE_TYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_COVERPAGE_TYPE_ENUM
 - faxcomex/FAX_COVERPAGE_TYPE_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_COVERPAGE_TYPE_ENUM
---

# FAX_COVERPAGE_TYPE_ENUM enumeration


## -description

The <b>FAX_COVERPAGE_TYPE_ENUM</b> enumeration defines whether a cover page template file is a local computer cover page or a server-based cover page. It can also specify that no file is used.

## -enum-fields

### -field fcptNONE:0

No cover page.

### -field fcptLOCAL

Use a cover page from local computer.

### -field fcptSERVER

Use a cover page from the fax server common coverpages folder.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-coverpagetype-vb">IFaxDocument::get_CoverPageType</a>
