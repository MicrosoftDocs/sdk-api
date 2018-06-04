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

# ImmGetImeMenuItemsW function


## -description


Retrieves the menu items that are registered in the IME menu of a specified input context.


## -parameters




### -param HIMC

TBD


### -param DWORD

TBD


### -param lpImeParentMenu [out, optional]

Pointer to an <a href="https://msdn.microsoft.com/2e00993f-6720-4139-8097-a3d830e661ca">IMEMENUITEMINFO</a> structure in which the function retrieves parent menu information. To retrieve information about the submenu items of this parent menu, the application sets the <b>fType</b> member to MFT_SUBMENU. This parameter contains <b>NULL</b> if the function retrieves only top-level menu items.


### -param lpImeMenu [out, optional]

Pointer to an array of <a href="https://msdn.microsoft.com/2e00993f-6720-4139-8097-a3d830e661ca">IMEMENUITEMINFO</a> structures in which the function retrieves information about the menu items. This parameter contains <b>NULL</b> if the function retrieves the number of registered menu items.


### -param dwSize [in]

Size of the buffer to receive the <a href="https://msdn.microsoft.com/2e00993f-6720-4139-8097-a3d830e661ca">IMEMENUITEMINFO</a> structure.


#### - dwFlags [in]

Flag specifying menu information options. The following value is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IGIMIF_RIGHTMENU"></a><a id="igimif_rightmenu"></a><dl>
<dt><b>IGIMIF_RIGHTMENU</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items for the context menu, obtained by a right mouse click.

</td>
</tr>
</table>
 


#### - dwType [in]

Type of menu to retrieve. This parameter can have one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IGIMII_CMODE"></a><a id="igimii_cmode"></a><dl>
<dt><b>IGIMII_CMODE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that control conversion mode.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_SMODE"></a><a id="igimii_smode"></a><dl>
<dt><b>IGIMII_SMODE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that control sentence mode.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_CONFIGURE"></a><a id="igimii_configure"></a><dl>
<dt><b>IGIMII_CONFIGURE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that are related to IME configuration.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_TOOLS"></a><a id="igimii_tools"></a><dl>
<dt><b>IGIMII_TOOLS</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that are related to IME tools.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_HELP"></a><a id="igimii_help"></a><dl>
<dt><b>IGIMII_HELP</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that control IME Help.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_OTHER"></a><a id="igimii_other"></a><dl>
<dt><b>IGIMII_OTHER</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that control other IME functions.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_INPUTTOOLS"></a><a id="igimii_inputtools"></a><dl>
<dt><b>IGIMII_INPUTTOOLS</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that control menu items related to IME input tools providing an extended way to input characters.

</td>
</tr>
</table>
 


#### - hIMC [in]

Handle to the input context for the specified menu items.


## -returns



Returns the number of menu items copied into <i>lpImeMenu</i>. If <i>lpImeMenu</i> specifies <b>NULL</b>, the function returns the number of registered menu items in the specified input context.




## -see-also




<a href="https://msdn.microsoft.com/2e00993f-6720-4139-8097-a3d830e661ca">IMEMENUITEMINFO</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

