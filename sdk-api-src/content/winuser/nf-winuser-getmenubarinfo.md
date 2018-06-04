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

# GetMenuBarInfo function


## -description


Retrieves information about the specified menu bar.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window (menu bar) whose information is to be retrieved. 


### -param idObject [in]

Type: <b>LONG</b>

The menu object. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OBJID_CLIENT"></a><a id="objid_client"></a><dl>
<dt><b>OBJID_CLIENT</b></dt>
<dt>((LONG)0xFFFFFFFC)</dt>
</dl>
</td>
<td width="60%">
The popup menu associated with the window.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJID_MENU"></a><a id="objid_menu"></a><dl>
<dt><b>OBJID_MENU</b></dt>
<dt>((LONG)0xFFFFFFFD)</dt>
</dl>
</td>
<td width="60%">
The menu bar associated with the window (see the <a href="https://msdn.microsoft.com/e86b20c6-9a4b-40b7-95d1-ffa57795f5e0">GetMenu</a> function).

</td>
</tr>
<tr>
<td width="40%"><a id="OBJID_SYSMENU"></a><a id="objid_sysmenu"></a><dl>
<dt><b>OBJID_SYSMENU</b></dt>
<dt>((LONG)0xFFFFFFFF)</dt>
</dl>
</td>
<td width="60%">
The system menu associated with the window (see the <a href="https://msdn.microsoft.com/a9b8456e-e849-44f9-9a3a-a059141d79b0">GetSystemMenu</a> function).

</td>
</tr>
</table>
 


### -param idItem [in]

Type: <b>LONG</b>

The item for which to retrieve information. If this parameter is zero, the function retrieves information about the menu itself. If this parameter is 1, the function retrieves information about the first item on the menu, and so on. 


### -param pmbi [in, out]

Type: <b>PMENUBARINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/1c6cdc30-5d0b-4b05-aaea-4ef62c4145c4">MENUBARINFO</a> structure that receives the information. Note that you must set the <b>cbSize</b> member to <code>sizeof(MENUBARINFO)</code> before calling this function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e86b20c6-9a4b-40b7-95d1-ffa57795f5e0">GetMenu</a>



<a href="https://msdn.microsoft.com/a9b8456e-e849-44f9-9a3a-a059141d79b0">GetSystemMenu</a>



<a href="https://msdn.microsoft.com/1c6cdc30-5d0b-4b05-aaea-4ef62c4145c4">MENUBARINFO</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

