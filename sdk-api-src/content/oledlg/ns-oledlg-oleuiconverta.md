---
UID: NS:oledlg.tagOLEUICONVERTA
title: OLEUICONVERTA (oledlg.h)
description: Contains information that the OLE User Interface Library uses to initialize the Convert dialog box, and space for the library to return information when the dialog box is dismissed. (ANSI)
helpviewer_keywords: ["*LPOLEUICONVERTA","*POLEUICONVERTA","CF_CONVERTONLY","CF_DISABLEACTIVATEAS","CF_DISABLEDISPLAYASICON","CF_HIDECHANGEICON","CF_SELECTACTIVATEAS","CF_SELECTCONVERTTO","CF_SETACTIVATEDEFAULT","CF_SETCONVERTDEFAULT","CF_SHOWHELPBUTTON","LPOLEUICONVERT","LPOLEUICONVERT structure pointer [COM]","OLEUICONVERT","OLEUICONVERT structure [COM]","OLEUICONVERTA","OLEUICONVERTW","POLEUICONVERT","POLEUICONVERT structure pointer [COM]","_ole_OLEUICONVERT_str","com.oleuiconvert_struct","oledlg/LPOLEUICONVERT","oledlg/OLEUICONVERT","oledlg/OLEUICONVERTA","oledlg/OLEUICONVERTW","oledlg/POLEUICONVERT"]
old-location: com\oleuiconvert_struct.htm
tech.root: com
ms.assetid: 79206f06-b219-48c2-9fb2-74ebc2dbac65
ms.date: 12/05/2018
ms.keywords: '*LPOLEUICONVERTA, *POLEUICONVERTA, CF_CONVERTONLY, CF_DISABLEACTIVATEAS, CF_DISABLEDISPLAYASICON, CF_HIDECHANGEICON, CF_SELECTACTIVATEAS, CF_SELECTCONVERTTO, CF_SETACTIVATEDEFAULT, CF_SETCONVERTDEFAULT, CF_SHOWHELPBUTTON, LPOLEUICONVERT, LPOLEUICONVERT structure pointer [COM], OLEUICONVERT, OLEUICONVERT structure [COM], OLEUICONVERTA, OLEUICONVERTW, POLEUICONVERT, POLEUICONVERT structure pointer [COM], _ole_OLEUICONVERT_str, com.oleuiconvert_struct, oledlg/LPOLEUICONVERT, oledlg/OLEUICONVERT, oledlg/OLEUICONVERTA, oledlg/OLEUICONVERTW, oledlg/POLEUICONVERT'
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUICONVERTW (Unicode) and OLEUICONVERTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLEUICONVERTA, *POLEUICONVERTA, *LPOLEUICONVERTA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUICONVERTA
 - oledlg/tagOLEUICONVERTA
 - POLEUICONVERTA
 - oledlg/POLEUICONVERTA
 - OLEUICONVERTA
 - oledlg/OLEUICONVERTA
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
 - OLEUICONVERT
 - OLEUICONVERTA
 - OLEUICONVERTW
---

# OLEUICONVERTA structure


## -description

Contains information that the OLE User Interface Library uses to initialize the <b>Convert</b> dialog box, and space for the library to return information when the dialog box is dismissed.

## -struct-fields

### -field cbStruct

The size of the structure, in bytes. This member must be filled on input.

### -field dwFlags

On input, this field specifies the initialization and creation flags. On exit, it specifies the user's choices. It may be a combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CF_SHOWHELPBUTTON"></a><a id="cf_showhelpbutton"></a><dl>
<dt><b>CF_SHOWHELPBUTTON</b></dt>
</dl>
</td>
<td width="60%">
Dialog box will display a <b>Help</b> button. This flag is set on input. 

</td>
</tr>
<tr>
<td width="40%"><a id="CF_SETCONVERTDEFAULT"></a><a id="cf_setconvertdefault"></a><dl>
<dt><b>CF_SETCONVERTDEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Class whose CLSID is specified by <b>clsidConvertDefault</b> will be used as the default selection. This selection appears in the class listbox when the <b>Convert To</b> radio button is selected. This flag is set on input. 


</td>
</tr>
<tr>
<td width="40%"><a id="CF_SETACTIVATEDEFAULT"></a><a id="cf_setactivatedefault"></a><dl>
<dt><b>CF_SETACTIVATEDEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Class whose CLSID is specified by <b>clsidActivateDefault</b> will be used as the default selection. This selection appears in the class listbox when the <b>Activate As</b> radio button is selected. This flag is set on input. 


</td>
</tr>
<tr>
<td width="40%"><a id="CF_SELECTCONVERTTO"></a><a id="cf_selectconvertto"></a><dl>
<dt><b>CF_SELECTCONVERTTO</b></dt>
</dl>
</td>
<td width="60%">
On input, this flag specifies that <b>Convert To</b> will be initially selected (default behavior). This flag is set on output if <b>Convert To</b> was selected when the user dismissed the dialog box. 


</td>
</tr>
<tr>
<td width="40%"><a id="CF_SELECTACTIVATEAS"></a><a id="cf_selectactivateas"></a><dl>
<dt><b>CF_SELECTACTIVATEAS</b></dt>
</dl>
</td>
<td width="60%">
On input, this flag specifies that <b>Activate As</b> will be initially selected. This flag is set on output if <b>Activate As</b> was selected when the user dismissed the dialog box. 


</td>
</tr>
<tr>
<td width="40%"><a id="CF_DISABLEDISPLAYASICON"></a><a id="cf_disabledisplayasicon"></a><dl>
<dt><b>CF_DISABLEDISPLAYASICON</b></dt>
</dl>
</td>
<td width="60%">
The <b>Display As Icon</b> button will be disabled on initialization. 


</td>
</tr>
<tr>
<td width="40%"><a id="CF_DISABLEACTIVATEAS"></a><a id="cf_disableactivateas"></a><dl>
<dt><b>CF_DISABLEACTIVATEAS</b></dt>
</dl>
</td>
<td width="60%">
The <b>Activate As</b> radio button will be disabled on initialization.

</td>
</tr>
<tr>
<td width="40%"><a id="CF_HIDECHANGEICON"></a><a id="cf_hidechangeicon"></a><dl>
<dt><b>CF_HIDECHANGEICON</b></dt>
</dl>
</td>
<td width="60%">
The <b>Change Icon</b> button will be hidden in the <b>Convert</b> dialog box. 


</td>
</tr>
<tr>
<td width="40%"><a id="CF_CONVERTONLY"></a><a id="cf_convertonly"></a><dl>
<dt><b>CF_CONVERTONLY</b></dt>
</dl>
</td>
<td width="60%">
The <b>Activate As</b> radio button will be disabled in the <b>Convert</b> dialog box. 




</td>
</tr>
</table>

### -field hWndOwner

The window that owns the dialog box. This member should not be <b>NULL</b>.

### -field lpszCaption

Pointer to a string to be used as the title of the dialog box. If <b>NULL</b>, then the library uses <b>Convert</b>.

### -field lpfnHook

Pointer to a hook function that processes messages intended for the dialog box. The hook function must return zero to pass a message that it didn't process back to the dialog box procedure in the library. The hook function must return a nonzero value to prevent the library's dialog box procedure from processing a message it has already processed.

### -field lCustData

Application-defined data that the library passes to the hook function pointed to by the <b>lpfnHook</b> member. The library passes a pointer to the <b>OLEUICONVERT</b> structure in the <i>lParam</i> parameter of the WM_INITDIALOG message; this pointer can be used to retrieve the <b>lCustData</b> member.

### -field hInstance

Instance that contains a dialog box template specified by the <b>lpszTemplate</b> member. This member is ignored if the <b>lpszTemplate</b> member is <b>NULL</b> or invalid.

### -field lpszTemplate

Pointer to a null-terminated string that specifies the name of the resource file for the dialog box template that is to be substituted for the library's <b>Convert</b> dialog box template.

### -field hResource

Resource handle for a custom dialog box. If this member is <b>NULL</b>, then the library uses the standard <b>Convert</b> dialog box template, or if it is valid, the template named by the <b>lpszTemplate</b> member.

### -field clsidConvertDefault

The CLSID to use as the default class when <b>Convert To</b> is selected. This member is ignored if the <b>dwFlags</b> member does not include CF_SETCONVERTDEFAULT. This member is set on input.

### -field clsidActivateDefault

The CLSID to use as the default class when <b>Activate As</b> is selected. This member is ignored if the <b>dwFlags</b> member does not include CF_SETACTIVATEDEFAULT. This member is set on input.

### -field clsidNew

The CLSID of the selected class. This member is set on output.

### -field clsid

The CLSID of the object to be converted or activated. This member is set on input.

### -field dvAspect

Aspect of the object. This must be either DVASPECT_CONTENT or DVASPECT_ICON. If <b>dvAspect</b> is DVASPECT_ICON on input, then the <b>Display As Icon</b> box is checked and the object's icon is displayed. This member is set on input and output. For more information, see <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>.

### -field wFormat

Data format of the object to be converted or activated.

### -field fIsLinkedObject

<b>TRUE</b> if the object is linked. This member is set on input.

### -field hMetaPict

The <a href="/windows/desktop/api/wingdi/ns-wingdi-metafilepict">METAFILEPICT</a> containing the iconic aspect. This member is set on input and output.

### -field lpszUserType

Pointer to the User Type name of the object to be converted or activated. If this value is <b>NULL</b>, then the dialog box will retrieve the User Type name from the registry. This string is freed on exit.

### -field fObjectsIconChanged

<b>TRUE</b> if the object's icon changed. (that is, if <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuichangeicona">OleUIChangeIcon</a> was called and not canceled.). This member is set on output.

### -field lpszDefLabel

Pointer to the default label to use for the icon. If <b>NULL</b>, the short user type name will be used. If the object is a link, the caller should pass the display name of the link source. This is freed on exit.

### -field cClsidExclude

Number of CLSIDs in <i>lpClsidExclude</i>.

### -field lpClsidExclude

Pointer to the list of CLSIDs to exclude from the list.

## -see-also

<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuichangeicona">OleUIChangeIcon</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiconverta">OleUIConvert</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines OLEUICONVERT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
