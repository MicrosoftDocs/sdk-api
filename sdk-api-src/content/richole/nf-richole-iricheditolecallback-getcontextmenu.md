---
UID: NF:richole.IRichEditOleCallback.GetContextMenu
title: IRichEditOleCallback::GetContextMenu
author: windows-sdk-content
description: Queries the application for a context menu to use on a right-click event.
old-location: controls\IRichEditOleCallback_GetContextMenu.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackgetcontextmenu.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GCM_RIGHTMOUSEDROP, GetContextMenu, GetContextMenu method [Windows Controls], GetContextMenu method [Windows Controls],IRichEditOleCallback interface, IRichEditOleCallback interface [Windows Controls],GetContextMenu method, IRichEditOleCallback.GetContextMenu, IRichEditOleCallback::GetContextMenu, SEL_EMPTY, SEL_MULTICHAR, SEL_MULTIOBJECT, SEL_OBJECT, SEL_TEXT, _win32_IRichEditOleCallback_GetContextMenu, _win32_IRichEditOleCallback_GetContextMenu_cpp, controls.IRichEditOleCallback_GetContextMenu, controls._win32_IRichEditOleCallback_GetContextMenu, richole/IRichEditOleCallback::GetContextMenu
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: richole.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TEXTRANGEW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOleCallback.GetContextMenu
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: ADAM
---

# IRichEditOleCallback::GetContextMenu


## -description


Queries the application for a context menu to use on a right-click event.


## -parameters




### -param seltype

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

Selection type. The value, which specifies the contents of the new selection, can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SEL_EMPTY"></a><a id="sel_empty"></a><dl>
<dt><b>SEL_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The selection is empty.

</td>
</tr>
<tr>
<td width="40%"><a id="SEL_TEXT"></a><a id="sel_text"></a><dl>
<dt><b>SEL_TEXT</b></dt>
</dl>
</td>
<td width="60%">
Text.

</td>
</tr>
<tr>
<td width="40%"><a id="SEL_OBJECT"></a><a id="sel_object"></a><dl>
<dt><b>SEL_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
At least one COM object.

</td>
</tr>
<tr>
<td width="40%"><a id="SEL_MULTICHAR"></a><a id="sel_multichar"></a><dl>
<dt><b>SEL_MULTICHAR</b></dt>
</dl>
</td>
<td width="60%">
More than one character of text.

</td>
</tr>
<tr>
<td width="40%"><a id="SEL_MULTIOBJECT"></a><a id="sel_multiobject"></a><dl>
<dt><b>SEL_MULTIOBJECT</b></dt>
</dl>
</td>
<td width="60%">
More than one COM object.

</td>
</tr>
<tr>
<td width="40%"><a id="GCM_RIGHTMOUSEDROP"></a><a id="gcm_rightmousedrop"></a><dl>
<dt><b>GCM_RIGHTMOUSEDROP</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a context menu for a right-mouse drag drop should be generated. The <i>lpoleobj</i> parameter is a pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface for the object being dropped.

</td>
</tr>
</table>
 


### -param lpoleobj

Type: <b>LPOLEOBJECT</b>

Pointer to an interface. If the 
					<i>seltype</i> parameter includes the <b>SEL_OBJECT</b> flag, 
					<i>lpoleobj</i> is a pointer to the <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> interface for the first selected COM object. If 
					<i>seltype</i> includes the <b>GCM_RIGHTMOUSEDROP</b> flag, 
					<i>lpoleobj</i> is a pointer to an 
					<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface. Otherwise, 
					<i>lpoleobj</i> is <b>NULL</b>. If you hold on to the interface pointer, you must call 
					the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method to increment the object's reference count. 


### -param lpchrg

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb787885(v=VS.85).aspx">CHARRANGE</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb787885(v=VS.85).aspx">CHARRANGE</a> structure containing the current selection. 


### -param lphmenu

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMENU</a>*</b>

The handle of a context menu to use. This parameter is ignored if an error is returned. A rich edit control destroys the menu when it is finished with it so the client should not. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns <b>S_OK</b> on success. If the method fails, it can be the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
There was an invalid argument.

</td>
</tr>
</table>
 




## -remarks



When the user selects an item from the context window, a <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> message is sent to the parent window of the rich edit control.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787885(v=VS.85).aspx">CHARRANGE</a>



<a href="https://msdn.microsoft.com/6354921F-3C9F-4CBD-AC48-1EB67D1FDEB7">GETCONTEXTMENUEX</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774308(v=VS.85).aspx">IRichEditOleCallback</a>



<b>Reference</b>
 

 

