---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagOLEUIBUSYA structure


## -description


Contains information that the OLE User Interface Library uses to initialize the <b>Busy</b> dialog box, and space for the library to return information when the dialog box is dismissed.


## -struct-fields




### -field cbStruct

The size of the structure, in bytes. This field must be filled on input.


### -field dwFlags

On input, specifies the initialization and creation flags. On exit, it specifies the user's choices. It may be a combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BZ_DISABLECANCELBUTTON"></a><a id="bz_disablecancelbutton"></a><dl>
<dt><b>BZ_DISABLECANCELBUTTON</b></dt>
</dl>
</td>
<td width="60%">
This flag disables the <b>Cancel</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="BZ_DISABLESWITCHTOBUTTON"></a><a id="bz_disableswitchtobutton"></a><dl>
<dt><b>BZ_DISABLESWITCHTOBUTTON</b></dt>
</dl>
</td>
<td width="60%">
Input only. This flag disables the <b>Switch To...</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="BZ_DISABLERETRYBUTTON"></a><a id="bz_disableretrybutton"></a><dl>
<dt><b>BZ_DISABLERETRYBUTTON</b></dt>
</dl>
</td>
<td width="60%">
Input only. This flag disables the <b>Retry</b> button. 

</td>
</tr>
<tr>
<td width="40%"><a id="BZ_NOTRESPONDINGDIALOG"></a><a id="bz_notrespondingdialog"></a><dl>
<dt><b>BZ_NOTRESPONDINGDIALOG</b></dt>
</dl>
</td>
<td width="60%">
Input only. This flag generates a <b>Not Responding</b> dialog box instead of a <b>Busy</b> dialog box. The text is slightly different, and the <b>Cancel</b> button is disabled.

</td>
</tr>
</table>
 


### -field hWndOwner

The window that owns the dialog box. This member should not be <b>NULL</b>.


### -field lpszCaption

A pointer to a string to be used as the title of the dialog box. If <b>NULL</b>, then the library uses <b>Busy</b>.


### -field lpfnHook

Pointer to a hook function that processes messages intended for the dialog box. The hook function must return zero to pass a message that it didn't process back to the dialog box procedure in the library. The hook function must return a nonzero value to prevent the library's dialog box procedure from processing a message it has already processed. 


### -field lCustData

Application-defined data that the library passes to the hook function pointed to by the <b>lpfnHook</b> member. The library passes a pointer to the <b>OLEUIBUSY</b> structure in the <i>lParam</i> parameter of the WM_INITDIALOG message; this pointer can be used to retrieve the <b>lCustData</b> member. 


### -field hInstance

Instance that contains a dialog box template specified by the <b>lpTemplateName</b> member.


### -field lpszTemplate

Pointer to a null-terminated string that specifies the name of the resource file for the dialog box template that is to be substituted for the library's <b>Busy</b> dialog box template.


### -field hResource

Customized template handle.


### -field hTask

Input only. Handle to the task that is blocking.


### -field lphWndDialog

Pointer to the dialog box's <b>HWND</b>.



## -see-also




<a href="https://msdn.microsoft.com/317f0dbf-7ac9-4e5a-a5ed-e6b807f07fb2">OleUIBusy</a>
 

 

