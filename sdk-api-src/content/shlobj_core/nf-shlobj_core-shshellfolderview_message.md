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

# SHShellFolderView_Message function


## -description


<p class="CCE_Message">[<b>SHShellFolderView_Message</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sends a message to the shell's default <a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a> implementation (DefView).


## -parameters




### -param hwndMain [in]

Type: <b>HWND</b>

A handle to the window that receives the message.


### -param uMsg

Type: <b>UINT</b>

The message to send. The following is a list of possible messages.

						

<table class="clsStd">
<tr>
<th>Message</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/90394af6-3809-457c-b2f2-5f35187ed45b">SFVM_ADDOBJECT</a>
</td>
<td>Adds an object to the shell view.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad">SFVM_GETSELECTEDOBJECTS</a>
</td>
<td>Retrieves an array of PIDLs for all selected objects.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/d745bafc-f2f5-40a1-b7e8-e16e4cf0153d">SFVM_REARRANGE</a>
</td>
<td>Notifies the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> to rearrange its items.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5b493cea-dfbd-4aee-8126-b118c058bb4c">SFVM_REMOVEOBJECT</a>
</td>
<td>Removes an object from the shell view.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e">SFVM_SETCLIPBOARD</a>
</td>
<td>Notifies the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> when one of its objects is placed on the clipboard as a result of a menu command.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b89f2d62-095b-4cad-a47e-2d41e122cb3e">SFVM_SETITEMPOS</a>
</td>
<td>Sets the position of an item in the shell view.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/d2c3e06a-19e4-4b78-9b7c-1a256582786e">SFVM_SETPOINTS</a>
</td>
<td>Sets the points of the currently selected objects to the data object on <b>copy</b> and <b>cut</b> commands.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3bd68ace-3ccf-446c-8cf9-52f42444674e">SFVM_UPDATEOBJECT</a>
</td>
<td>Updates an object by passing a pointer to an array of two PIDLs.</td>
</tr>
</table>
 


### -param lParam

Type: <b>LPARAM</b>

Contents of this value depend on the message passed in <i>uMsg</i>. See individual message topics for more information.


## -returns



Type: <b>LRESULT</b>

The return value depends on the message passed in <i>uMsg</i>. See individual message topics for more information.




## -see-also




<a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a>
 

 

