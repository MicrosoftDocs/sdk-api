---
UID: NS:oledlg.tagOLEUICHANGESOURCEW
title: OLEUICHANGESOURCEW (oledlg.h)
description: Contains information that is used to initialize the standard Change Source dialog box. (Unicode)
helpviewer_keywords: ["*LPOLEUICHANGESOURCEW","*POLEUICHANGESOURCEW","CSF_ONLYGETSOURCE","CSF_SHOWHELP","CSF_VALIDSOURCE","LPOLEUICHANGESOURCE","LPOLEUICHANGESOURCE structure pointer [COM]","OLEUICHANGESOURCE","OLEUICHANGESOURCE structure [COM]","OLEUICHANGESOURCEA","OLEUICHANGESOURCEW","POLEUICHANGESOURCE","POLEUICHANGESOURCE structure pointer [COM]","_ole_OLEUICHANGESOURCE_str","com.oleuichangesource_struct","oledlg/LPOLEUICHANGESOURCE","oledlg/OLEUICHANGESOURCE","oledlg/OLEUICHANGESOURCEA","oledlg/OLEUICHANGESOURCEW","oledlg/POLEUICHANGESOURCE"]
old-location: com\oleuichangesource_struct.htm
tech.root: com
ms.assetid: 440d120c-a121-471b-bee1-f23af136a664
ms.date: 12/05/2018
ms.keywords: '*LPOLEUICHANGESOURCEW, *POLEUICHANGESOURCEW, CSF_ONLYGETSOURCE, CSF_SHOWHELP, CSF_VALIDSOURCE, LPOLEUICHANGESOURCE, LPOLEUICHANGESOURCE structure pointer [COM], OLEUICHANGESOURCE, OLEUICHANGESOURCE structure [COM], OLEUICHANGESOURCEA, OLEUICHANGESOURCEW, POLEUICHANGESOURCE, POLEUICHANGESOURCE structure pointer [COM], _ole_OLEUICHANGESOURCE_str, com.oleuichangesource_struct, oledlg/LPOLEUICHANGESOURCE, oledlg/OLEUICHANGESOURCE, oledlg/OLEUICHANGESOURCEA, oledlg/OLEUICHANGESOURCEW, oledlg/POLEUICHANGESOURCE'
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUICHANGESOURCEW (Unicode) and OLEUICHANGESOURCEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLEUICHANGESOURCEW, *POLEUICHANGESOURCEW, *LPOLEUICHANGESOURCEW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUICHANGESOURCEW
 - oledlg/tagOLEUICHANGESOURCEW
 - POLEUICHANGESOURCEW
 - oledlg/POLEUICHANGESOURCEW
 - OLEUICHANGESOURCEW
 - oledlg/OLEUICHANGESOURCEW
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
 - OLEUICHANGESOURCE
 - OLEUICHANGESOURCEA
 - OLEUICHANGESOURCEW
---

# OLEUICHANGESOURCEW structure


## -description

Contains information that is used to initialize the standard <b>Change Source</b> dialog box. It allows the user to modify the destination or source of a link. This may simply entail selecting a different file name for the link, or possibly changing the item reference within the file, for example, changing the destination range of cells within the spreadsheet that the link is to.

## -struct-fields

### -field cbStruct

The size of the structure, in bytes.

### -field dwFlags

On input, this field specifies the initialization and creation flags. On exit, it specifies the user's choices. It may be a combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CSF_SHOWHELP"></a><a id="csf_showhelp"></a><dl>
<dt><b>CSF_SHOWHELP</b></dt>
</dl>
</td>
<td width="60%">
 Enables or shows the Help button. 


</td>
</tr>
<tr>
<td width="40%"><a id="CSF_VALIDSOURCE"></a><a id="csf_validsource"></a><dl>
<dt><b>CSF_VALIDSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the link was validated.

</td>
</tr>
<tr>
<td width="40%"><a id="CSF_ONLYGETSOURCE"></a><a id="csf_onlygetsource"></a><dl>
<dt><b>CSF_ONLYGETSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Disables automatic validation of the link source when the user presses <b>OK</b>. If you specify this flag, you should validate the source when the dialog box returns <b>OK</b>. 


</td>
</tr>
</table>

### -field hWndOwner

The window that owns the dialog box.

### -field lpszCaption

Pointer to a string to be used as the title of the dialog box. If <b>NULL</b>, then the library uses <b>Change Source</b>.

### -field lpfnHook

Pointer to a hook function that processes messages intended for the dialog box. The hook function must return zero to pass a message that it didn't process back to the dialog box procedure in the library. The hook function must return a nonzero value to prevent the library's dialog box procedure from processing a message it has already processed.

### -field lCustData

Application-defined data that the library passes to the hook function pointed to by the [OLEUICHANGEICON](./nf-oledlg-oleuichangeicona.md) structure in the <i>lParam</i> parameter of the WM_INITDIALOG message; this pointer can be used to retrieve the <b>lCustData</b> member.

### -field hInstance

Instance that contains a dialog box template specified by the <b>lpszTemplate</b> member. This member is ignored if the <b>lpszTemplate</b> member is <b>NULL</b> or invalid.

### -field lpszTemplate

Pointer to a null-terminated string that specifies the name of the resource file for the dialog box template that is to be substituted for the library's <b>Convert</b> dialog box template.

### -field hResource

Resource handle for a custom dialog box. If this member is <b>NULL</b>, then the library uses the standard <b>Convert</b> dialog box template, or if it is valid, the template named by the <b>lpszTemplate</b> member.

### -field lpOFN

Pointer to the <a href="/windows/win32/api/commdlg/ns-commdlg-openfilenamea">OPENFILENAME</a> structure, which contains information used by the operating system to initialize the system-defined <b>Open</b> or <b>Save As</b> dialog boxes.

### -field dwReserved1

This member is reserved.

### -field lpOleUILinkContainer

Pointer to the container's implementation of the <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a> interface, used to validate the link source. The <b>Edit Links</b> dialog box uses this to allow the container to manipulate its links.

### -field dwLink

Container-defined unique link identifier used to validate link sources. Used by <b>lpOleUILinkContainer</b>.

### -field lpszDisplayName

Pointer to the complete source display name.

### -field nFileLength

File moniker portion of <b>lpszDisplayName</b>.

### -field lpszFrom

Pointer to the prefix of the source that was changed from.

### -field lpszTo

Pointer to the prefix of the source to be changed to.

## -see-also

<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuichangesourcea">OleUIChangeSource</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines OLEUICHANGESOURCE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
