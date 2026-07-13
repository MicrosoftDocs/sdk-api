---
UID: NS:oledlg.tagOLEUIVIEWPROPSW
title: OLEUIVIEWPROPSW (oledlg.h)
description: Contains information that is used to initialize the View tab of the Object properties dialog box. (Unicode)
helpviewer_keywords: ["*LPOLEUIVIEWPROPSW","*POLEUIVIEWPROPSW","LPOLEUIVIEWPROPS","LPOLEUIVIEWPROPS structure pointer [COM]","OLEUIVIEWPROPS","OLEUIVIEWPROPS structure [COM]","OLEUIVIEWPROPSA","OLEUIVIEWPROPSW","POLEUIVIEWPROPS","POLEUIVIEWPROPS structure pointer [COM]","VPF_DISABLERELATIVE","VPF_DISABLESCALE","VPF_SELECTRELATIVE","_ole_OLEUIVIEWPROPS","com.oleuiviewprops_struct","oledlg/LPOLEUIVIEWPROPS","oledlg/OLEUIVIEWPROPS","oledlg/OLEUIVIEWPROPSA","oledlg/OLEUIVIEWPROPSW","oledlg/POLEUIVIEWPROPS"]
old-location: com\oleuiviewprops_struct.htm
tech.root: com
ms.assetid: e45565c5-185e-4143-a5c2-d0b273b5086e
ms.date: 12/05/2018
ms.keywords: '*LPOLEUIVIEWPROPSW, *POLEUIVIEWPROPSW, LPOLEUIVIEWPROPS, LPOLEUIVIEWPROPS structure pointer [COM], OLEUIVIEWPROPS, OLEUIVIEWPROPS structure [COM], OLEUIVIEWPROPSA, OLEUIVIEWPROPSW, POLEUIVIEWPROPS, POLEUIVIEWPROPS structure pointer [COM], VPF_DISABLERELATIVE, VPF_DISABLESCALE, VPF_SELECTRELATIVE, _ole_OLEUIVIEWPROPS, com.oleuiviewprops_struct, oledlg/LPOLEUIVIEWPROPS, oledlg/OLEUIVIEWPROPS, oledlg/OLEUIVIEWPROPSA, oledlg/OLEUIVIEWPROPSW, oledlg/POLEUIVIEWPROPS'
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIVIEWPROPSW (Unicode) and OLEUIVIEWPROPSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLEUIVIEWPROPSW, *POLEUIVIEWPROPSW, *LPOLEUIVIEWPROPSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUIVIEWPROPSW
 - oledlg/tagOLEUIVIEWPROPSW
 - POLEUIVIEWPROPSW
 - oledlg/POLEUIVIEWPROPSW
 - OLEUIVIEWPROPSW
 - oledlg/OLEUIVIEWPROPSW
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
 - OLEUIVIEWPROPS
 - OLEUIVIEWPROPSA
 - OLEUIVIEWPROPSW
---

# OLEUIVIEWPROPSW structure


## -description

Contains information that is used to initialize the <b>View</b> tab of the <b>Object properties</b> dialog box. A reference to it is passed in as part of the <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiobjectpropsa">OLEUIOBJECTPROPS</a> structure to the <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiobjectpropertiesa">OleUIObjectProperties</a> function. This tab allows the user to toggle between "content" and "iconic" views of the object, and change its scaling within the container. It also allows the user to tunnel to the change icon dialog box when the object is being displayed iconically.

## -struct-fields

### -field cbStruct

The size of the structure, in bytes.

### -field dwFlags

Flags specific to view page.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VPF_SELECTRELATIVE"></a><a id="vpf_selectrelative"></a><dl>
<dt><b>VPF_SELECTRELATIVE</b></dt>
</dl>
</td>
<td width="60%">
Relative to origin.

</td>
</tr>
<tr>
<td width="40%"><a id="VPF_DISABLERELATIVE"></a><a id="vpf_disablerelative"></a><dl>
<dt><b>VPF_DISABLERELATIVE</b></dt>
</dl>
</td>
<td width="60%">
Disable relative to origin.

</td>
</tr>
<tr>
<td width="40%"><a id="VPF_DISABLESCALE"></a><a id="vpf_disablescale"></a><dl>
<dt><b>VPF_DISABLESCALE</b></dt>
</dl>
</td>
<td width="60%">
Disable scale option.

</td>
</tr>
</table>

### -field dwReserved1

This member is reserved.

### -field lpfnHook

Pointer to a hook callback (not used in this dialog box).

### -field lCustData

Custom data to pass to the hook (not used in this dialog box).

### -field dwReserved2

This member is reserved.

### -field lpOP

Used internally.

### -field nScaleMin

Minimum value for the scale range.

### -field nScaleMax

Maximum value for the scale range.

## -see-also

<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiobjectpropsa">OLEUIOBJECTPROPS</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines OLEUIVIEWPROPS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
