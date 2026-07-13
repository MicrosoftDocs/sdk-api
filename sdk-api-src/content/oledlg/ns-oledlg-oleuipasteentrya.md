---
UID: NS:oledlg.tagOLEUIPASTEENTRYA
title: OLEUIPASTEENTRYA (oledlg.h)
description: An array of entries to be specified in the OLEUIPASTESPECIAL structure for the Paste Special dialog box. (ANSI)
helpviewer_keywords: ["*LPOLEUIPASTEENTRYA","*POLEUIPASTEENTRYA","LPOLEUIPASTEENTRY","LPOLEUIPASTEENTRY structure pointer [COM]","OLEUIPASTEENTRY","OLEUIPASTEENTRY structure [COM]","OLEUIPASTEENTRYA","OLEUIPASTEENTRYW","POLEUIPASTEENTRY","POLEUIPASTEENTRY structure pointer [COM]","_ole_OLEUIPASTEENTRY","com.oleuipasteentry_struct","oledlg/LPOLEUIPASTEENTRY","oledlg/OLEUIPASTEENTRY","oledlg/OLEUIPASTEENTRYA","oledlg/OLEUIPASTEENTRYW","oledlg/POLEUIPASTEENTRY"]
old-location: com\oleuipasteentry_struct.htm
tech.root: com
ms.assetid: 9c84bb0e-d998-4e35-bf34-2377f5cd0cb7
ms.date: 12/05/2018
ms.keywords: '*LPOLEUIPASTEENTRYA, *POLEUIPASTEENTRYA, LPOLEUIPASTEENTRY, LPOLEUIPASTEENTRY structure pointer [COM], OLEUIPASTEENTRY, OLEUIPASTEENTRY structure [COM], OLEUIPASTEENTRYA, OLEUIPASTEENTRYW, POLEUIPASTEENTRY, POLEUIPASTEENTRY structure pointer [COM], _ole_OLEUIPASTEENTRY, com.oleuipasteentry_struct, oledlg/LPOLEUIPASTEENTRY, oledlg/OLEUIPASTEENTRY, oledlg/OLEUIPASTEENTRYA, oledlg/OLEUIPASTEENTRYW, oledlg/POLEUIPASTEENTRY'
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIPASTEENTRYW (Unicode) and OLEUIPASTEENTRYA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLEUIPASTEENTRYA, *POLEUIPASTEENTRYA, *LPOLEUIPASTEENTRYA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUIPASTEENTRYA
 - oledlg/tagOLEUIPASTEENTRYA
 - POLEUIPASTEENTRYA
 - oledlg/POLEUIPASTEENTRYA
 - OLEUIPASTEENTRYA
 - oledlg/OLEUIPASTEENTRYA
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
 - OLEUIPASTEENTRY
 - OLEUIPASTEENTRYA
 - OLEUIPASTEENTRYW
---

# OLEUIPASTEENTRYA structure


## -description

An array of entries to be specified in the <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipastespeciala">OLEUIPASTESPECIAL</a> structure for the <b>Paste Special</b> dialog box. Each entry includes a <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure which specifies the formats that are acceptable, a string that is to represent the format in the dialog box's listbox, a string to customize the result text of the dialog box, and a set of flags from the <a href="/windows/desktop/api/oledlg/ne-oledlg-oleuipasteflag">OLEUIPASTEFLAG</a> enumeration. The flags indicate if the entry is valid for pasting only, linking only or both pasting and linking. If the entry is valid for linking, the flags indicate which link types are acceptable by OR'ing together the appropriate OLEUIPASTE_LINKTYPE<i>n</i> values.

## -struct-fields

### -field fmtetc

Format that is acceptable. The <b>Paste Special</b> dialog box checks if this format is offered by the object on the clipboard and if so, offers it for selection to the user.

### -field lpstrFormatName

Pointer to the string that represents the format to the user. Any %s in this string is replaced by the FullUserTypeName of the object on the clipboard and the resulting string is placed in the list box of the dialog box. Only one %s is allowed. The presence or absence of %s specifies whether the result-text is to indicate that data is being pasted or that an object that can be activated by an application is being pasted. If %s is present, the resulting text says that an object is being pasted. Otherwise, it says that data is being pasted.

### -field lpstrResultText

Pointer to the string used to customize the resulting text of the dialog box when the user selects the format corresponding to this entry. Any %s in this string is replaced by the application name or FullUserTypeName of the object on the clipboard. Only one %s is allowed.

### -field dwFlags

Values from <a href="/windows/desktop/api/oledlg/ne-oledlg-oleuipasteflag">OLEUIPASTEFLAG</a> enumeration.

### -field dwScratchSpace

Scratch space available to routines that loop through an <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> to mark if the PasteEntry format is available. This field can be left uninitialized.

## -see-also

<a href="/windows/desktop/api/oledlg/ne-oledlg-oleuipasteflag">OLEUIPASTEFLAG</a>



<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipastespeciala">OLEUIPASTESPECIAL</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuipastespeciala">OleUIPasteSpecial</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines OLEUIPASTEENTRY as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
