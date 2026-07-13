---
UID: NS:oledlg.tagOLEUIEDITLINKSA
title: OLEUIEDITLINKSA (oledlg.h)
description: Contains information that the OLE User Interface Library uses to initialize the Edit Links dialog box, and contains space for the library to return information when the dialog box is dismissed. (ANSI)
helpviewer_keywords: ["*LPOLEUIEDITLINKSA","*POLEUIEDITLINKSA","ELF_DISABLECANCELLINK","ELF_DISABLECHANGESOURCE","ELF_DISABLEOPENSOURCE","ELF_DISABLEUPDATENOW","ELF_SHOWHELP","LPOLEUIEDITLINKS","LPOLEUIEDITLINKS structure pointer [COM]","OLEUIEDITLINKS","OLEUIEDITLINKS structure [COM]","OLEUIEDITLINKSA","OLEUIEDITLINKSW","POLEUIEDITLINKS","POLEUIEDITLINKS structure pointer [COM]","_ole_OLEUIEDITLINKS_str","com.oleuieditlinks_struct","oledlg/LPOLEUIEDITLINKS","oledlg/OLEUIEDITLINKS","oledlg/OLEUIEDITLINKSA","oledlg/OLEUIEDITLINKSW","oledlg/POLEUIEDITLINKS"]
old-location: com\oleuieditlinks_struct.htm
tech.root: com
ms.assetid: 0a139936-bda4-40c8-85d6-b52ff042f2d9
ms.date: 12/05/2018
ms.keywords: '*LPOLEUIEDITLINKSA, *POLEUIEDITLINKSA, ELF_DISABLECANCELLINK, ELF_DISABLECHANGESOURCE, ELF_DISABLEOPENSOURCE, ELF_DISABLEUPDATENOW, ELF_SHOWHELP, LPOLEUIEDITLINKS, LPOLEUIEDITLINKS structure pointer [COM], OLEUIEDITLINKS, OLEUIEDITLINKS structure [COM], OLEUIEDITLINKSA, OLEUIEDITLINKSW, POLEUIEDITLINKS, POLEUIEDITLINKS structure pointer [COM], _ole_OLEUIEDITLINKS_str, com.oleuieditlinks_struct, oledlg/LPOLEUIEDITLINKS, oledlg/OLEUIEDITLINKS, oledlg/OLEUIEDITLINKSA, oledlg/OLEUIEDITLINKSW, oledlg/POLEUIEDITLINKS'
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIEDITLINKSW (Unicode) and OLEUIEDITLINKSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLEUIEDITLINKSA, *POLEUIEDITLINKSA, *LPOLEUIEDITLINKSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEUIEDITLINKSA
 - oledlg/tagOLEUIEDITLINKSA
 - POLEUIEDITLINKSA
 - oledlg/POLEUIEDITLINKSA
 - OLEUIEDITLINKSA
 - oledlg/OLEUIEDITLINKSA
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
 - OLEUIEDITLINKS
 - OLEUIEDITLINKSA
 - OLEUIEDITLINKSW
---

# OLEUIEDITLINKSA structure


## -description

Contains information that the OLE User Interface Library uses to initialize the <b>Edit Links</b> dialog box, and contains space for the library to return information when the dialog box is dismissed.

## -struct-fields

### -field cbStruct

The size of the structure, in bytes. This member must be filled on input.

### -field dwFlags

On input, <b>dwFlags</b> specifies the initialization and creation flags. It may be a combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ELF_SHOWHELP"></a><a id="elf_showhelp"></a><dl>
<dt><b>ELF_SHOWHELP</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the dialog box will display a <b>Help</b> button. 


</td>
</tr>
<tr>
<td width="40%"><a id="ELF_DISABLEUPDATENOW"></a><a id="elf_disableupdatenow"></a><dl>
<dt><b>ELF_DISABLEUPDATENOW</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the <b>Update Now</b> button will be disabled on initialization.

</td>
</tr>
<tr>
<td width="40%"><a id="ELF_DISABLEOPENSOURCE"></a><a id="elf_disableopensource"></a><dl>
<dt><b>ELF_DISABLEOPENSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the <b>Open Source</b> button will be disabled on initialization.

</td>
</tr>
<tr>
<td width="40%"><a id="ELF_DISABLECHANGESOURCE"></a><a id="elf_disablechangesource"></a><dl>
<dt><b>ELF_DISABLECHANGESOURCE</b></dt>
</dl>
</td>
<td width="60%">
 Specifies that the <b>Change Source</b> button will be disabled on initialization.

</td>
</tr>
<tr>
<td width="40%"><a id="ELF_DISABLECANCELLINK"></a><a id="elf_disablecancellink"></a><dl>
<dt><b>ELF_DISABLECANCELLINK</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the <b>Cancel Link</b> button will be disabled on initialization. 


</td>
</tr>
</table>

### -field hWndOwner

The window that owns the dialog box. This member should not be <b>NULL</b>.

### -field lpszCaption

Pointer to a string to be used as the title of the dialog box. If <b>NULL</b>, then the library uses <b>Links</b>.

### -field lpfnHook

Pointer to a hook function that processes messages intended for the dialog box. The hook function must return zero to pass a message that it didn't process back to the dialog box procedure in the library. The hook function must return a nonzero value to prevent the library's dialog box procedure from processing a message it has already processed.

### -field lCustData

Application-defined data that the library passes to the hook function pointed to by the <b>lpfnHook</b> member. The library passes a pointer to the <b>OLEUIEDITLINKS</b> structure in the <i>lParam</i> parameter of the WM_INITDIALOG message; this pointer can be used to retrieve the <b>lCustData</b> member.

### -field hInstance

Instance that contains a dialog box template specified by the <b>lpTemplateName</b> member.

### -field lpszTemplate

Pointer to a null-terminated string that specifies the name of the resource file for the dialog box template that is to be substituted for the library's <b>Edit Links</b> dialog box template.

### -field hResource

Customized template handle.

### -field lpOleUILinkContainer

Pointer to the container's implementation of the <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a> Interface. The <b>Edit Links</b> dialog box uses this to allow the container to manipulate its links.

## -see-also

<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a>

## -remarks

> [!NOTE]
> The oledlg.h header defines OLEUIEDITLINKS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
