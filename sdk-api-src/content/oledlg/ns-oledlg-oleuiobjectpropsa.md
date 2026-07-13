---
UID: NS:oledlg.tagOLEUIOBJECTPROPSA
title: OLEUIOBJECTPROPSA (oledlg.h)
description: Contains information that is used to initialize the standard Object Properties dialog box. (ANSI)
helpviewer_keywords: ["*LPOLEUIOBJECTPROPSA","*POLEUIOBJECTPROPSA","LPOLEUIOBJECTPROPS","LPOLEUIOBJECTPROPS structure pointer [COM]","OLEUIOBJECTPROPS","OLEUIOBJECTPROPS structure [COM]","OLEUIOBJECTPROPSA","OLEUIOBJECTPROPSW","OPF_DISABLECONVERT","OPF_NOFILLDEFAULT","OPF_OBJECTISLINK","OPF_SHOWHELP","POLEUIOBJECTPROPS","POLEUIOBJECTPROPS structure pointer [COM]","_ole_OLEUIOBJECTPROPS","com.oleuiobjectprops_struct","oledlg/LPOLEUIOBJECTPROPS","oledlg/OLEUIOBJECTPROPS","oledlg/OLEUIOBJECTPROPSA","oledlg/OLEUIOBJECTPROPSW","oledlg/POLEUIOBJECTPROPS"]
old-location: com\oleuiobjectprops_struct.htm
tech.root: com
ms.assetid: 7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3
ms.date: 12/05/2018
ms.keywords: '*LPOLEUIOBJECTPROPSA, *POLEUIOBJECTPROPSA, LPOLEUIOBJECTPROPS, LPOLEUIOBJECTPROPS structure pointer [COM], OLEUIOBJECTPROPS, OLEUIOBJECTPROPS structure [COM], OLEUIOBJECTPROPSA, OLEUIOBJECTPROPSW, OPF_DISABLECONVERT, OPF_NOFILLDEFAULT, OPF_OBJECTISLINK, OPF_SHOWHELP, POLEUIOBJECTPROPS, POLEUIOBJECTPROPS structure pointer [COM], _ole_OLEUIOBJECTPROPS, com.oleuiobjectprops_struct, oledlg/LPOLEUIOBJECTPROPS, oledlg/OLEUIOBJECTPROPS, oledlg/OLEUIOBJECTPROPSA, oledlg/OLEUIOBJECTPROPSW, oledlg/POLEUIOBJECTPROPS'
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIOBJECTPROPSW (Unicode) and OLEUIOBJECTPROPSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLEUIOBJECTPROPSA, *POLEUIOBJECTPROPSA, *LPOLEUIOBJECTPROPSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUIOBJECTPROPSA
 - oledlg/tagOLEUIOBJECTPROPSA
 - POLEUIOBJECTPROPSA
 - oledlg/POLEUIOBJECTPROPSA
 - OLEUIOBJECTPROPSA
 - oledlg/OLEUIOBJECTPROPSA
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
 - OLEUIOBJECTPROPS
 - OLEUIOBJECTPROPSA
 - OLEUIOBJECTPROPSW
---

# OLEUIOBJECTPROPSA structure


## -description

Contains information that is used to initialize the standard <b>Object Properties</b> dialog box. It contains references to interfaces used to gather information about the embedding or link, references to three structures that are used to initialize the default tabs - <b>General</b> (<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuignrlpropsa">OLEUIGNRLPROPS</a>), <b>View</b> (<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiviewpropsa">OLEUIVIEWPROPS</a>), and <b>Link</b> (<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuilinkpropsa">OLEUILINKPROPS</a>), if appropriate - and a standard property-sheet extensibility interface that allows the caller to add additional custom property sheets to the dialog box.

## -struct-fields

### -field cbStruct

The size of the structure, in bytes.

### -field dwFlags

Contains in/out global flags for the property sheet.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OPF_OBJECTISLINK"></a><a id="opf_objectislink"></a><dl>
<dt><b>OPF_OBJECTISLINK</b></dt>
</dl>
</td>
<td width="60%">
Object is a link object and therefore has a link property page.

</td>
</tr>
<tr>
<td width="40%"><a id="OPF_NOFILLDEFAULT"></a><a id="opf_nofilldefault"></a><dl>
<dt><b>OPF_NOFILLDEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Do not fill in default values for the object.

</td>
</tr>
<tr>
<td width="40%"><a id="OPF_SHOWHELP"></a><a id="opf_showhelp"></a><dl>
<dt><b>OPF_SHOWHELP</b></dt>
</dl>
</td>
<td width="60%">
The dialog box will display a <b>Help</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="OPF_DISABLECONVERT"></a><a id="opf_disableconvert"></a><dl>
<dt><b>OPF_DISABLECONVERT</b></dt>
</dl>
</td>
<td width="60%">
The <b>Convert</b> button will be disabled on the general property page.

</td>
</tr>
</table>

### -field lpPS

Pointer to the standard property sheet header (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PROPSHEETHEADER</a>), used for extensibility.

### -field dwObject

Identifier for the object.

### -field lpObjInfo

Pointer to the interface to manipulate object.

### -field dwLink

Container-defined unique identifier for a single link. Containers can use the pointer to the link's container site for this value.

### -field lpLinkInfo

 Pointer to the interface to manipulate link.

### -field lpGP

 Pointer to the general page data.

### -field lpVP

Pointer to the view page data.

### -field lpLP

Pointer to the link page data.

## -see-also

<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuignrlpropsa">OLEUIGNRLPROPS</a>



<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuilinkpropsa">OLEUILINKPROPS</a>



<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiviewpropsa">OLEUIVIEWPROPS</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiobjectpropertiesa">OleUIObjectProperties</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines OLEUIOBJECTPROPS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
