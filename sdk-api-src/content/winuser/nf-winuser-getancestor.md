---
UID: NF:winuser.GetAncestor
title: GetAncestor function
author: windows-sdk-content
description: Retrieves the handle to the ancestor of the specified window.
old-location: winmsg\getancestor.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getancestor.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GA_PARENT, GA_ROOT, GA_ROOTOWNER, GetAncestor, GetAncestor function [Windows and Messages], _win32_GetAncestor, _win32_getancestor_cpp, winmsg.getancestor, winui._win32_getancestor, winuser/GetAncestor
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetAncestor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetAncestor function


## -description


Retrieves the handle to the ancestor of the specified window. 


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window whose ancestor is to be retrieved. If this parameter is the desktop window, the function returns <b>NULL</b>. 


### -param gaFlags [in]

Type: <b>UINT</b>

The ancestor to be retrieved. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GA_PARENT"></a><a id="ga_parent"></a><dl>
<dt><b>GA_PARENT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Retrieves the parent window. This does not include the owner, as it does with the <a href="https://msdn.microsoft.com/en-us/library/ms633510(v=VS.85).aspx">GetParent</a> function. 

</td>
</tr>
<tr>
<td width="40%"><a id="GA_ROOT"></a><a id="ga_root"></a><dl>
<dt><b>GA_ROOT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Retrieves the root window by walking the chain of parent windows.

</td>
</tr>
<tr>
<td width="40%"><a id="GA_ROOTOWNER"></a><a id="ga_rootowner"></a><dl>
<dt><b>GA_ROOTOWNER</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Retrieves the owned root window by walking the chain of parent and owner windows returned by <a href="https://msdn.microsoft.com/en-us/library/ms633510(v=VS.85).aspx">GetParent</a>. 

</td>
</tr>
</table>
 


## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

The return value is the handle to the ancestor window.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633510(v=VS.85).aspx">GetParent</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

