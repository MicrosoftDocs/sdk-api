---
UID: NE:oledlg.tagOLEUIPASTEFLAG
title: OLEUIPASTEFLAG (oledlg.h)
description: Indicates the user options that are available to the user when pasting this format, and within which group or list of choices (Paste, Paste Link, etc.).
helpviewer_keywords: ["OLEUIPASTEFLAG","OLEUIPASTEFLAG enumeration [COM]","OLEUIPASTE_ENABLEICON","OLEUIPASTE_LINKANYTYPE","OLEUIPASTE_LINKTYPE1","OLEUIPASTE_LINKTYPE2","OLEUIPASTE_LINKTYPE3","OLEUIPASTE_LINKTYPE4","OLEUIPASTE_LINKTYPE5","OLEUIPASTE_LINKTYPE6","OLEUIPASTE_LINKTYPE7","OLEUIPASTE_LINKTYPE8","OLEUIPASTE_PASTE","OLEUIPASTE_PASTEONLY","_ole_OLEUIPASTEFLAG","com.oleuipasteflag","oledlg/OLEUIPASTEFLAG","oledlg/OLEUIPASTE_ENABLEICON","oledlg/OLEUIPASTE_LINKANYTYPE","oledlg/OLEUIPASTE_LINKTYPE1","oledlg/OLEUIPASTE_LINKTYPE2","oledlg/OLEUIPASTE_LINKTYPE3","oledlg/OLEUIPASTE_LINKTYPE4","oledlg/OLEUIPASTE_LINKTYPE5","oledlg/OLEUIPASTE_LINKTYPE6","oledlg/OLEUIPASTE_LINKTYPE7","oledlg/OLEUIPASTE_LINKTYPE8","oledlg/OLEUIPASTE_PASTE","oledlg/OLEUIPASTE_PASTEONLY"]
old-location: com\oleuipasteflag.htm
tech.root: com
ms.assetid: 4467f82b-34be-4d10-816c-b3e4231c92a1
ms.date: 12/05/2018
ms.keywords: OLEUIPASTEFLAG, OLEUIPASTEFLAG enumeration [COM], OLEUIPASTE_ENABLEICON, OLEUIPASTE_LINKANYTYPE, OLEUIPASTE_LINKTYPE1, OLEUIPASTE_LINKTYPE2, OLEUIPASTE_LINKTYPE3, OLEUIPASTE_LINKTYPE4, OLEUIPASTE_LINKTYPE5, OLEUIPASTE_LINKTYPE6, OLEUIPASTE_LINKTYPE7, OLEUIPASTE_LINKTYPE8, OLEUIPASTE_PASTE, OLEUIPASTE_PASTEONLY, _ole_OLEUIPASTEFLAG, com.oleuipasteflag, oledlg/OLEUIPASTEFLAG, oledlg/OLEUIPASTE_ENABLEICON, oledlg/OLEUIPASTE_LINKANYTYPE, oledlg/OLEUIPASTE_LINKTYPE1, oledlg/OLEUIPASTE_LINKTYPE2, oledlg/OLEUIPASTE_LINKTYPE3, oledlg/OLEUIPASTE_LINKTYPE4, oledlg/OLEUIPASTE_LINKTYPE5, oledlg/OLEUIPASTE_LINKTYPE6, oledlg/OLEUIPASTE_LINKTYPE7, oledlg/OLEUIPASTE_LINKTYPE8, oledlg/OLEUIPASTE_PASTE, oledlg/OLEUIPASTE_PASTEONLY
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: OLEUIPASTEFLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUIPASTEFLAG
 - oledlg/tagOLEUIPASTEFLAG
 - OLEUIPASTEFLAG
 - oledlg/OLEUIPASTEFLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleDlg.h
api_name:
 - OLEUIPASTEFLAG
---

# OLEUIPASTEFLAG enumeration


## -description

Indicates the user options that are available to the user when pasting this format, and within which group or list of choices (<b>Paste</b>, <b>Paste Link</b>, etc.).

## -enum-fields

### -field OLEUIPASTE_ENABLEICON:2048

If the container does not specify this flag for the entry in the <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipasteentrya">OLEUIPASTEENTRY</a> array passed as input to <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuipastespeciala">OleUIPasteSpecial</a>, the DisplayAsIcon button will be unchecked and disabled when the user selects the format that corresponds to the entry.

### -field OLEUIPASTE_PASTEONLY:0

The entry in the <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipasteentrya">OLEUIPASTEENTRY</a> array is valid for pasting only.

### -field OLEUIPASTE_PASTE:512

The entry in the <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipasteentrya">OLEUIPASTEENTRY</a> array is valid for pasting. It may also be valid for linking if any of the following linking flags are specified. If it is valid for linking, then the following flags indicate which link types are acceptable by OR'ing together the appropriate OLEUIPASTE_LINKTYPE<i>n</i> values. These values correspond as follows to the array of link types passed to <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuipastespeciala">OleUIPasteSpecial</a> in the <b>arrLinkTypes</b> member of the <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipastespeciala">OLEUIPASTESPECIAL</a> structure:

<ul>
<li>OLEUIPASTE_LINKTYPE1=arrLinkTypes[0]</li>
<li>OLEUIPASTE_LINKTYPE2=arrLinkTypes[1]</li>
<li>OLEUIPASTE_LINKTYPE3=arrLinkTypes[2]</li>
<li>OLEUIPASTE_LINKTYPE4=arrLinkTypes[3]</li>
<li>OLEUIPASTE_LINKTYPE5=arrLinkTypes[4]</li>
<li>OLEUIPASTE_LINKTYPE6=arrLinkTypes[5]</li>
<li>OLEUIPASTE_LINKTYPE7=arrLinkTypes[6]</li>
<li>OLEUIPASTE_LINKTYPE8=arrLinkTypes[7]</li>
</ul>
The <b>arrLinkTypes</b> array is an array of registered clipboard formats for linking. A maximum of 8 link types is allowed.

### -field OLEUIPASTE_LINKANYTYPE:1024

Any link type.

### -field OLEUIPASTE_LINKTYPE1:1

Link type 1.

### -field OLEUIPASTE_LINKTYPE2:2

Link type 2.

### -field OLEUIPASTE_LINKTYPE3:4

Link type 3.

### -field OLEUIPASTE_LINKTYPE4:8

Link type 4.

### -field OLEUIPASTE_LINKTYPE5:16

Link type 5.

### -field OLEUIPASTE_LINKTYPE6:32

Link type 6.

### -field OLEUIPASTE_LINKTYPE7:64

Link type 7.

### -field OLEUIPASTE_LINKTYPE8:128

Link type 8.

## -see-also

<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipasteentrya">OLEUIPASTEENTRY</a>
