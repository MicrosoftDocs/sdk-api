---
UID: NS:oledlg.tagOLEUICHANGEICONW
title: tagOLEUICHANGEICONW
author: windows-driver-content
description: Contains information that the OLE User Interface Library uses to initialize the Change Icon dialog box, and it contains space for the library to return information when the dialog box is dismissed.
old-location: com\oleuichangeicon_struct.htm
old-project: com
ms.assetid: 2c4ba340-541a-405b-889c-bc51d1d20cc9
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: "*LPOLEUICHANGEICONW, *POLEUICHANGEICONW, CIF_SELECTCURRENT, CIF_SELECTDEFAULT, CIF_SELECTFROMFILE, CIF_SHOWHELP, CIF_USEICONEXE, LPOLEUICHANGEICON, LPOLEUICHANGEICON structure pointer [COM], OLEUICHANGEICON, OLEUICHANGEICON structure [COM], OLEUICHANGEICONW, POLEUICHANGEICON, POLEUICHANGEICON structure pointer [COM], _ole_OLEUICHANGEICON_str, com.oleuichangeicon_struct, oledlg/LPOLEUICHANGEICON, oledlg/POLEUICHANGEICON, oledlg/tagOLEUICHANGEICON, oledlg/tagOLEUICHANGEICONA, oledlg/tagOLEUICHANGEICONW, tagOLEUICHANGEICON, tagOLEUICHANGEICON structure [COM], tagOLEUICHANGEICONA, tagOLEUICHANGEICONW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: tagOLEUICHANGEICONW (Unicode) and tagOLEUICHANGEICONA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OLEUICHANGEICONW, *POLEUICHANGEICONW, *LPOLEUICHANGEICONW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	OleDlg.h
api_name:
-	OLEUICHANGEICON
-	tagOLEUICHANGEICONA
-	tagOLEUICHANGEICONW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagOLEUICHANGEICONW structure


## -description


Contains information that the OLE User Interface Library uses to initialize the <b>Change Icon</b> dialog box, and it contains space for the library to return information when the dialog box is dismissed.


## -struct-fields




### -field cbStruct

The size of the structure, in bytes. This field must be filled on input.


### -field dwFlags

On input, specifies the initialization and creation flags. On exit, it specifies the user's choices. It can be a combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CIF_SHOWHELP"></a><a id="cif_showhelp"></a><dl>
<dt><b>CIF_SHOWHELP</b></dt>
</dl>
</td>
<td width="60%">
Dialog box will display a <b>Help</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="CIF_SELECTCURRENT"></a><a id="cif_selectcurrent"></a><dl>
<dt><b>CIF_SELECTCURRENT</b></dt>
</dl>
</td>
<td width="60%">
On input, selects the <b>Current</b> radio button on initialization. On exit, specifies that the user selected <b>Current</b>.


</td>
</tr>
<tr>
<td width="40%"><a id="CIF_SELECTDEFAULT"></a><a id="cif_selectdefault"></a><dl>
<dt><b>CIF_SELECTDEFAULT</b></dt>
</dl>
</td>
<td width="60%">
On input, selects the <b>Default</b> radio button on initialization. On exit, specifies that the user selected <b>Default</b>.




</td>
</tr>
<tr>
<td width="40%"><a id="CIF_SELECTFROMFILE"></a><a id="cif_selectfromfile"></a><dl>
<dt><b>CIF_SELECTFROMFILE</b></dt>
</dl>
</td>
<td width="60%">
On input, selects the <b>From File</b> radio button on initialization. On exit, specifies that the user selected <b>From File</b>.




</td>
</tr>
<tr>
<td width="40%"><a id="CIF_USEICONEXE"></a><a id="cif_useiconexe"></a><dl>
<dt><b>CIF_USEICONEXE</b></dt>
</dl>
</td>
<td width="60%">
 Input only. Extracts the icon from the executable specified in the <b>szIconExe</b> member, instead of retrieving it from the class. This is useful for OLE embedding or linking to non-OLE files.


</td>
</tr>
</table>
 


### -field hWndOwner

The window that owns the dialog box. This member should not be <b>NULL</b>.


### -field lpszCaption

Pointer to a string to be used as the title of the dialog box. If <b>NULL</b>, then the library uses <b>Change Icon</b>.


### -field lpfnHook

Pointer to a hook function that processes messages intended for the dialog box. The hook function must return zero to pass a message that it didn't process back to the dialog box procedure in the library. The hook function must return a nonzero value to prevent the library's dialog box procedure from processing a message it has already processed. 


### -field lCustData

Application-defined data that the library passes to the hook function pointed to by the <b>lpfnHook</b> member. The library passes a pointer to the <b>OLEUICHANGEICON</b> structure in the lParam parameter of the WM_INITDIALOG message; this pointer can be used to retrieve the <b>lCustData</b> member. 


### -field hInstance

Instance that contains a dialog box template specified by the <b>lpTemplateName</b> member. 


### -field lpszTemplate

Pointer to a null-terminated string that specifies the name of the resource file for the dialog box template that is to be substituted for the library's <b>Change Icon</b> dialog box template. 


### -field hResource

Customized template handle.


### -field hMetaPict

Current and final image. The source of the icon is embedded in the metafile itself.


### -field clsid

Input only. The class to use to get the <b>Default</b> icon.


### -field szIconExe

Input only. Pointer to the executable to extract the default icon from. This member is ignored unless CIF_USEICONEXE is included in the <b>dwFlags</b> member and an attempt to retrieve the class icon from the specified CLSID fails. 


### -field cchIconExe

Input only. The number of characters in <b>szIconExe</b>. This member is ignored unless CIF_USEICONEXE is included in the <b>dwFlags</b> member.



## -see-also




<a href="https://msdn.microsoft.com/899aadbe-d3d7-42e2-b9c0-09efeb378bda">OleUIChangeIcon</a>
 

 

