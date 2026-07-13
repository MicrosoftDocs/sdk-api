---
UID: NS:oledlg.tagOLEUILINKPROPSA
title: OLEUILINKPROPSA (oledlg.h)
description: Contains information that is used to initialize the Link tab of the Object Properties dialog box. (ANSI)
helpviewer_keywords: ["*LPOLEUILINKPROPSA","*POLEUILINKPROPSA","LPOLEUILINKPROPS","LPOLEUILINKPROPS structure pointer [COM]","OLEUILINKPROPS","OLEUILINKPROPS structure [COM]","OLEUILINKPROPSA","OLEUILINKPROPSW","POLEUILINKPROPS","POLEUILINKPROPS structure pointer [COM]","_ole_OLEUILINKPROPS","com.oleuilinkprops_struct","oledlg/LPOLEUILINKPROPS","oledlg/OLEUILINKPROPS","oledlg/OLEUILINKPROPSA","oledlg/OLEUILINKPROPSW","oledlg/POLEUILINKPROPS"]
old-location: com\oleuilinkprops_struct.htm
tech.root: com
ms.assetid: 3f355ce8-adc3-4878-a8b4-3f7d94547ef1
ms.date: 12/05/2018
ms.keywords: '*LPOLEUILINKPROPSA, *POLEUILINKPROPSA, LPOLEUILINKPROPS, LPOLEUILINKPROPS structure pointer [COM], OLEUILINKPROPS, OLEUILINKPROPS structure [COM], OLEUILINKPROPSA, OLEUILINKPROPSW, POLEUILINKPROPS, POLEUILINKPROPS structure pointer [COM], _ole_OLEUILINKPROPS, com.oleuilinkprops_struct, oledlg/LPOLEUILINKPROPS, oledlg/OLEUILINKPROPS, oledlg/OLEUILINKPROPSA, oledlg/OLEUILINKPROPSW, oledlg/POLEUILINKPROPS'
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUILINKPROPSW (Unicode) and OLEUILINKPROPSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLEUILINKPROPSA, *POLEUILINKPROPSA, *LPOLEUILINKPROPSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUILINKPROPSA
 - oledlg/tagOLEUILINKPROPSA
 - POLEUILINKPROPSA
 - oledlg/POLEUILINKPROPSA
 - OLEUILINKPROPSA
 - oledlg/OLEUILINKPROPSA
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
 - OLEUILINKPROPS
 - OLEUILINKPROPSA
 - OLEUILINKPROPSW
---

# OLEUILINKPROPSA structure


## -description

Contains information that is used to initialize the <b>Link</b> tab of the <b>Object Properties</b> dialog box. A reference to it is passed in as part of the <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiobjectpropsa">OLEUIOBJECTPROPS</a> structure to the <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiobjectpropertiesa">OleUIObjectProperties</a> function. This tab shows the location, update status, and update time for a link. It allows the user to change the source of the link, toggle its update status between automatic and manual update, open the source, force an update of the link, or break the link (convert it to a static picture).

## -struct-fields

### -field cbStruct

The size of the structure, in bytes.

### -field dwFlags

Contains in/out flags specific to the <b>Links</b> page.

### -field dwReserved1

This member is reserved.

### -field lpfnHook

Pointer to the hook callback (not used in this dialog box).

### -field lCustData

Custom data to pass to hook (not used in this dialog box).

### -field dwReserved2

This member is reserved.

### -field lpOP

Used internally.

## -see-also

<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiobjectpropsa">OLEUIOBJECTPROPS</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiobjectpropertiesa">OleUIObjectProperties</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines OLEUILINKPROPS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
