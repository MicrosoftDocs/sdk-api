---
UID: NS:oledlg.tagOLEUIPASTESPECIALW
title: OLEUIPASTESPECIALW (oledlg.h)
description: Contains information that the OLE User Interface Library uses to initialize the Paste Special dialog box, as well as space for the library to return information when the dialog box is dismissed. (Unicode)
helpviewer_keywords: ["*LPOLEUIPASTESPECIALW","*POLEUIPASTESPECIALW","HIDECHANGEICON","LPOLEUIPASTESPECIAL","LPOLEUIPASTESPECIAL structure pointer [COM]","NOREFRESHDATAOBJECT","OLEUIPASTESPECIAL","OLEUIPASTESPECIAL structure [COM]","OLEUIPASTESPECIALA","OLEUIPASTESPECIALW","POLEUIPASTESPECIAL","POLEUIPASTESPECIAL structure pointer [COM]","PSF_CHECKDISPLAYASICON","PSF_DISABLEDISPLAYASICON","PSF_SELECTPASTE","PSF_SELECTPASTELINK","PSF_SHOWHELP","STAYONCLIPBOARDCHANGE","_ole_OLEUIPASTESPECIAL_str","com.oleuipastespecial_struct","oledlg/LPOLEUIPASTESPECIAL","oledlg/OLEUIPASTESPECIAL","oledlg/OLEUIPASTESPECIALA","oledlg/OLEUIPASTESPECIALW","oledlg/POLEUIPASTESPECIAL"]
old-location: com\oleuipastespecial_struct.htm
tech.root: com
ms.assetid: bb346fa7-03ae-458d-8488-64db7a9c48e1
ms.date: 12/05/2018
ms.keywords: '*LPOLEUIPASTESPECIALW, *POLEUIPASTESPECIALW, HIDECHANGEICON, LPOLEUIPASTESPECIAL, LPOLEUIPASTESPECIAL structure pointer [COM], NOREFRESHDATAOBJECT, OLEUIPASTESPECIAL, OLEUIPASTESPECIAL structure [COM], OLEUIPASTESPECIALA, OLEUIPASTESPECIALW, POLEUIPASTESPECIAL, POLEUIPASTESPECIAL structure pointer [COM], PSF_CHECKDISPLAYASICON, PSF_DISABLEDISPLAYASICON, PSF_SELECTPASTE, PSF_SELECTPASTELINK, PSF_SHOWHELP, STAYONCLIPBOARDCHANGE, _ole_OLEUIPASTESPECIAL_str, com.oleuipastespecial_struct, oledlg/LPOLEUIPASTESPECIAL, oledlg/OLEUIPASTESPECIAL, oledlg/OLEUIPASTESPECIALA, oledlg/OLEUIPASTESPECIALW, oledlg/POLEUIPASTESPECIAL'
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIPASTESPECIALW (Unicode) and OLEUIPASTESPECIALA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLEUIPASTESPECIALW, *POLEUIPASTESPECIALW, *LPOLEUIPASTESPECIALW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUIPASTESPECIALW
 - oledlg/tagOLEUIPASTESPECIALW
 - POLEUIPASTESPECIALW
 - oledlg/POLEUIPASTESPECIALW
 - OLEUIPASTESPECIALW
 - oledlg/OLEUIPASTESPECIALW
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
 - OLEUIPASTESPECIAL
 - OLEUIPASTESPECIALA
 - OLEUIPASTESPECIALW
---

# OLEUIPASTESPECIALW structure


## -description

Contains information that the OLE User Interface Library uses to initialize the <b>Paste Special</b> dialog box, as well as space for the library to return information when the dialog box is dismissed.

## -struct-fields

### -field cbStruct

The size of the structure, in bytes. This member must be filled on input.

### -field dwFlags

On input, <b>dwFlags</b> specifies the initialization and creation flags. On exit, it specifies the user's choices. It may be a combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PSF_SHOWHELP"></a><a id="psf_showhelp"></a><dl>
<dt><b>PSF_SHOWHELP</b></dt>
</dl>
</td>
<td width="60%">
Dialog box will display a <b>Help</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSF_SELECTPASTE"></a><a id="psf_selectpaste"></a><dl>
<dt><b>PSF_SELECTPASTE</b></dt>
</dl>
</td>
<td width="60%">
The <b>Paste</b> radio button will be selected at dialog box startup. This is the default, if PSF_SELECTPASTE or PSF_SELECTPASTELINK are not specified. Also, it specifies the state of the button on dialog termination. IN/OUT flag. 


</td>
</tr>
<tr>
<td width="40%"><a id="PSF_SELECTPASTELINK"></a><a id="psf_selectpastelink"></a><dl>
<dt><b>PSF_SELECTPASTELINK</b></dt>
</dl>
</td>
<td width="60%">
The <b>PasteLink</b> radio button will be selected at dialog box startup. Also, specifies the state of the button on dialog termination. IN/OUT flag. 


</td>
</tr>
<tr>
<td width="40%"><a id="PSF_CHECKDISPLAYASICON"></a><a id="psf_checkdisplayasicon"></a><dl>
<dt><b>PSF_CHECKDISPLAYASICON</b></dt>
</dl>
</td>
<td width="60%">
Whether the <b>Display As Icon</b> radio button was checked on dialog box termination. OUT flag. 


</td>
</tr>
<tr>
<td width="40%"><a id="PSF_DISABLEDISPLAYASICON"></a><a id="psf_disabledisplayasicon"></a><dl>
<dt><b>PSF_DISABLEDISPLAYASICON</b></dt>
</dl>
</td>
<td width="60%">
The <b>Display As Icon</b> check box will be disabled on initialization.

</td>
</tr>
<tr>
<td width="40%"><a id="HIDECHANGEICON"></a><a id="hidechangeicon"></a><dl>
<dt><b>HIDECHANGEICON</b></dt>
</dl>
</td>
<td width="60%">
Used to disable the change-icon button in the dialog box, which is available to users when they're pasting an OLE object by default. See <b>STAYONCLIPBOARDCHANGE</b> otherwise. 


</td>
</tr>
<tr>
<td width="40%"><a id="STAYONCLIPBOARDCHANGE"></a><a id="stayonclipboardchange"></a><dl>
<dt><b>STAYONCLIPBOARDCHANGE</b></dt>
</dl>
</td>
<td width="60%">
 Used to tell the dialog box to stay up if the clipboard changes while the dialog box is up. If the user switches to another application and copies or cuts something, the dialog box will, by default, perform a cancel operation, which will remove the dialog box since the options it's in the middle of presenting to the user are no longer up-to-date with respect to what's really on the clipboard. 


</td>
</tr>
<tr>
<td width="40%"><a id="NOREFRESHDATAOBJECT"></a><a id="norefreshdataobject"></a><dl>
<dt><b>NOREFRESHDATAOBJECT</b></dt>
</dl>
</td>
<td width="60%">
 Used in conjunction with <b>STAYONCLIPBOARDCHANGE</b> (it doesn't do anything otherwise). If the clipboard changes while the dialog box is up and <b>STAYONCLIPBOARDCHANGE</b> is specified, then <b>NOREFRESHDATAOBJECT</b> indicates that the dialog box should NOT refresh the contents of the dialog box to reflect the new contents of the clipboard. This is useful if the application is using the paste-special dialog box on an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> besides the one on the clipboard, for example, as part of a right-click drag-and-drop operation. 


</td>
</tr>
</table>

### -field hWndOwner

The window that owns the dialog box. This member should not be <b>NULL</b>.

### -field lpszCaption

Pointer to a string to be used as the title of the dialog box. If <b>NULL</b>, then the library uses <b>Paste Special</b>.

### -field lpfnHook

Pointer to a hook function that processes messages intended for the dialog box. The hook function must return zero to pass a message that it didn't process back to the dialog box procedure in the library. The hook function must return a nonzero value to prevent the library's dialog box procedure from processing a message it has already processed.

### -field lCustData

Application-defined data that the library passes to the hook function pointed to by the <b>lpfnHook</b> member. The library passes a pointer to the <b>OLEUIPASTESPECIAL</b> structure in the <b>lParam</b> parameter of the WM_INITDIALOG message; this pointer can be used to retrieve the <b>lCustData</b> member.

### -field hInstance

Instance that contains a dialog box template specified by the <b>lpTemplateName</b> member.

### -field lpszTemplate

Pointer to a null-terminated string that specifies the name of the resource file for the dialog box template that is to be substituted for the library's <b>Paste Special</b> dialog box template.

### -field hResource

Customized template handle.

### -field lpSrcDataObj

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface of the data object to be pasted (from the clipboard). This member is filled on input. If <b>lpSrcDataObj</b> is <b>NULL</b> when <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuipastespeciala">OleUIPasteSpecial</a> is called, then <b>OleUIPasteSpecial</b> will attempt to retrieve a pointer to an <b>IDataObject</b> from the clipboard. If <b>OleUIPasteSpecial</b> succeeds, it is the caller's responsibility to free the <b>IDataObject</b> returned in <b>lpSrcDataObj</b>.

### -field arrPasteEntries

The <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipasteentrya">OLEUIPASTEENTRY</a> array which specifies acceptable formats. This member is filled on input.

### -field cPasteEntries

Number of <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipasteentrya">OLEUIPASTEENTRY</a> array entries. This member is filled on input.

### -field arrLinkTypes

List of link types that are acceptable. Link types are referred to using <a href="/windows/desktop/api/oledlg/ne-oledlg-oleuipasteflag">OLEUIPASTEFLAG</a> in <b>arrPasteEntries</b>. This member is filled on input.

### -field cLinkTypes

Number of link types. This member is filled on input.

### -field cClsidExclude

Number of CLSIDs in <b>lpClsidExclude</b>. This member is filled on input.

### -field lpClsidExclude

Pointer to an array of CLSIDs to exclude from the list of available server objects for a Paste operation. Note that this does not affect <b>Paste Link</b>. An application can prevent embedding into itself by listing its own CLSID in this list. This field is filled on input.

### -field nSelectedIndex

Index of <b>arrPasteEntries</b> that the user selected. This member is filled on output.

### -field fLink

Whether <b>Paste</b> or <b>Paste Link</b> was selected by the user. This member is filled on output.

### -field hMetaPict

Handle to the Metafile containing the icon and icon title selected by the user. This member is filled on output.

### -field sizel

The size of object as displayed in its source, if the display aspect chosen by the user matches the aspect displayed in the source. If the user chooses a different aspect, then <b>sizel.cx</b> and <b>sizel.cy</b> are both set to zero. The size of the object as it is displayed in the source is retrieved from the ObjectDescriptor if <b>fLink</b> is <b>FALSE</b> and from the LinkSrcDescriptor if <b>fLink</b> is <b>TRUE</b>. This member is filled on output.

## -see-also

<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipasteentrya">OLEUIPASTEENTRY</a>



<a href="/windows/desktop/api/oledlg/ne-oledlg-oleuipasteflag">OLEUIPASTEFLAG</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuipastespeciala">OleUIPasteSpecial</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines OLEUIPASTESPECIAL as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
