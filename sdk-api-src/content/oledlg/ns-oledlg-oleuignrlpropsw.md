---
UID: NS:oledlg.tagOLEUIGNRLPROPSW
title: OLEUIGNRLPROPSW (oledlg.h)
description: Initializes the General tab of the Object Properties dialog box. (Unicode)
helpviewer_keywords: ["*LPOLEUIGNRLPROPSW","*POLEUIGNRLPROPSW","LPOLEUIGNRLPROPS","LPOLEUIGNRLPROPS structure pointer [COM]","OLEUIGNRLPROPS","OLEUIGNRLPROPS structure [COM]","OLEUIGNRLPROPSA","OLEUIGNRLPROPSW","POLEUIGNRLPROPS","POLEUIGNRLPROPS structure pointer [COM]","_ole_OLEUIGNRLPROPS","com.oleuignrlprops_struct","oledlg/LPOLEUIGNRLPROPS","oledlg/OLEUIGNRLPROPS","oledlg/OLEUIGNRLPROPSA","oledlg/OLEUIGNRLPROPSW","oledlg/POLEUIGNRLPROPS"]
old-location: com\oleuignrlprops_struct.htm
tech.root: com
ms.assetid: 851d66c8-94a7-47ab-95f4-12a34897de20
ms.date: 12/05/2018
ms.keywords: '*LPOLEUIGNRLPROPSW, *POLEUIGNRLPROPSW, LPOLEUIGNRLPROPS, LPOLEUIGNRLPROPS structure pointer [COM], OLEUIGNRLPROPS, OLEUIGNRLPROPS structure [COM], OLEUIGNRLPROPSA, OLEUIGNRLPROPSW, POLEUIGNRLPROPS, POLEUIGNRLPROPS structure pointer [COM], _ole_OLEUIGNRLPROPS, com.oleuignrlprops_struct, oledlg/LPOLEUIGNRLPROPS, oledlg/OLEUIGNRLPROPS, oledlg/OLEUIGNRLPROPSA, oledlg/OLEUIGNRLPROPSW, oledlg/POLEUIGNRLPROPS'
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIGNRLPROPSW (Unicode) and OLEUIGNRLPROPSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLEUIGNRLPROPSW, *POLEUIGNRLPROPSW, *LPOLEUIGNRLPROPSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUIGNRLPROPSW
 - oledlg/tagOLEUIGNRLPROPSW
 - POLEUIGNRLPROPSW
 - oledlg/POLEUIGNRLPROPSW
 - OLEUIGNRLPROPSW
 - oledlg/OLEUIGNRLPROPSW
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
 - OLEUIGNRLPROPS
 - OLEUIGNRLPROPSA
 - OLEUIGNRLPROPSW
---

# OLEUIGNRLPROPSW structure


## -description

Initializes the <b>General</b> tab of the <b>Object Properties</b> dialog box. A reference to it is passed in as part of the <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiobjectpropsa">OLEUIOBJECTPROPS</a> structure to the <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiobjectpropertiesa">OleUIObjectProperties</a> function. This tab shows the type and size of an OLE embedding and allows it the user to tunnel to the <b>Convert</b> dialog box. This tab also shows the link destination if the object is a link.

## -struct-fields

### -field cbStruct

The size of the structure, in bytes. This field must be filled on input.

### -field dwFlags

Currently no flags associated with this member. It should be set to 0 (zero).

### -field dwReserved1

This member is reserved.

### -field lpfnHook

Pointer to a hook function that processes messages intended for the dialog box. The hook function must return zero to pass a message that it didn't process back to the dialog box procedure in the library. The hook function must return a nonzero value to prevent the library's dialog box procedure from processing a message it has already processed.

### -field lCustData

Application-defined data that the library passes to the hook function pointed to by the <b>lpfnHook</b> member during WM_INITDIALOG.

### -field dwReserved2

This member is reserved.

### -field lpOP

Used internally.

## -see-also

<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiobjectpropsa">OLEUIOBJECTPROPS</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiobjectpropertiesa">OleUIObjectProperties</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines OLEUIGNRLPROPS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
