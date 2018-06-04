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

# ImmAssociateContextEx function


## -description


Changes the association between the input method context and the specified window or its children.


## -parameters




### -param

TBD




#### - dwFlags [in]

Flags specifying the type of association between the window and the input method context. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IACE_CHILDREN"></a><a id="iace_children"></a><dl>
<dt><b>IACE_CHILDREN</b></dt>
</dl>
</td>
<td width="60%">
Associate the input method context to the child windows of the specified window only.

</td>
</tr>
<tr>
<td width="40%"><a id="IACE_DEFAULT"></a><a id="iace_default"></a><dl>
<dt><b>IACE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Restore the default input method context of the window.

</td>
</tr>
<tr>
<td width="40%"><a id="IACE_IGNORENOCONTEXT"></a><a id="iace_ignorenocontext"></a><dl>
<dt><b>IACE_IGNORENOCONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Do not associate the input method context with windows that are not associated with any input method context.

</td>
</tr>
</table>
 


#### - hIMC [in]

Handle to the input method context.


#### - hWnd [in]

Handle to the window to associate with the input context.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -remarks



If the application calls this function with IACE_CHILDREN, the operating system associates the specified input method context with child windows of the window indicated by <i>hWnd</i>. It associates the input method context only with child windows of the thread that creates <i>hWnd</i>. Any child window that is created after this function has been called will not be affected. Instead, the default input method context will be associated with it.

If the application calls this function with IACE_DEFAULT, the operating system restores the default input method context for the window. In this case, the <i>hIMC</i> parameter is ignored.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

