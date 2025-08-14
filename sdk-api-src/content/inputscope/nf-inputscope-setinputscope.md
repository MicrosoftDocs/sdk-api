---
UID: NF:inputscope.SetInputScope
title: SetInputScope function (inputscope.h)
description: Sets an input scope for the specified window.
helpviewer_keywords: ["SetInputScope","SetInputScope function [Text Services Framework]","inputscope/SetInputScope","tsf.SetInputScope"]
old-location: tsf\SetInputScope.htm
tech.root: TSF
ms.assetid: 4098525c-8d29-419a-9484-9e70420416bc
ms.date: 12/05/2018
ms.keywords: SetInputScope, SetInputScope function [Text Services Framework], inputscope/SetInputScope, tsf.SetInputScope
req.header: inputscope.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetInputScope
 - inputscope/SetInputScope
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-tsf-msctf-l1-1-4.dll
 - ext-ms-win-tsf-msctf-l1-1-3.dll
 - ext-ms-win-tsf-msctf-l1-1-2.dll
 - msctf.dll
 - Ext-MS-Win-Tsf-MSctf-l1-1-0.dll
 - Ext-MS-Win-Tsf-MSctf-L1-1-1.dll
api_name:
 - SetInputScope
---

# SetInputScope function


## -description

Sets an input scope for the specified window.

## -parameters

### -param hwnd [in]

The window to set the scope on.

### -param inputscope [in]

The input scope to associate with the window. To remove the input scope association, pass IS_DEFAULT to this parameter.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>The method was successful.</td>
</tr>
</table>

## -remarks

Calling this method replaces whatever scope is associated with the window.

An application must call this method, passing in IS_DEFAULT to the <i>hwnd</i> parameter, to remove the input scope association before the window is destroyed.

This API works only when the window (<i>hwnd</i> parameter) and the calling thread are in the same thread. If you call this API for a different thread's window, it fails with E_INVALIDARG.

If you call this method on a window (<i>hwnd</i> parameter) that has 
not been associated with a Document Manager, then no text service notifications are sent to interested clients (such as the touch keyboard) that may want to respond to the 
scope change.


#### Examples

[C++]

The following code illustrates how to set an input scope for a window.

<div class="code"></div>

```cpp

SetInputScope(hwnd, IS_EMAIL_USERNAME);

```

