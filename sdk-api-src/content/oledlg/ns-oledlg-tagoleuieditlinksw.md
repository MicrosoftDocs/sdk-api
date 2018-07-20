---
UID: NS:oledlg.tagOLEUIEDITLINKSW
title: tagOLEUIEDITLINKSW
author: windows-sdk-content
description: Contains information that the OLE User Interface Library uses to initialize the Edit Links dialog box, and contains space for the library to return information when the dialog box is dismissed.
old-location: com\oleuieditlinks_struct.htm
old-project: com
ms.assetid: 0a139936-bda4-40c8-85d6-b52ff042f2d9
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*LPOLEUIEDITLINKSW, *POLEUIEDITLINKSW, ELF_DISABLECANCELLINK, ELF_DISABLECHANGESOURCE, ELF_DISABLEOPENSOURCE, ELF_DISABLEUPDATENOW, ELF_SHOWHELP, LPOLEUIEDITLINKS, LPOLEUIEDITLINKS structure pointer [COM], OLEUIEDITLINKS, OLEUIEDITLINKS structure [COM], OLEUIEDITLINKSA, OLEUIEDITLINKSW, POLEUIEDITLINKS, POLEUIEDITLINKS structure pointer [COM], _ole_OLEUIEDITLINKS_str, com.oleuieditlinks_struct, oledlg/LPOLEUIEDITLINKS, oledlg/OLEUIEDITLINKS, oledlg/OLEUIEDITLINKSA, oledlg/OLEUIEDITLINKSW, oledlg/POLEUIEDITLINKS, tagOLEUIEDITLINKSW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: OLEUIEDITLINKSW, *POLEUIEDITLINKSW, *LPOLEUIEDITLINKSW
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagOLEUIEDITLINKSW structure


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

Pointer to the container's implementation of the <a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a> Interface. The <b>Edit Links</b> dialog box uses this to allow the container to manipulate its links.



## -see-also




<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a>
 

 

