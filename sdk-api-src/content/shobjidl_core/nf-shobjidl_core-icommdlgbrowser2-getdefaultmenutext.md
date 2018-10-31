---
UID: NF:shobjidl_core.ICommDlgBrowser2.GetDefaultMenuText
title: ICommDlgBrowser2::GetDefaultMenuText
author: windows-sdk-content
description: Called by the Shell view to get the default shortcut menu text.
old-location: shell\ICommDlgBrowser2_GetDefaultMenuText.htm
tech.root: shell
ms.assetid: 08c73959-d884-4870-9e6f-f1040184556f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetDefaultMenuText, GetDefaultMenuText method [Windows Shell], GetDefaultMenuText method [Windows Shell],ICommDlgBrowser2 interface, ICommDlgBrowser2 interface [Windows Shell],GetDefaultMenuText method, ICommDlgBrowser2.GetDefaultMenuText, ICommDlgBrowser2::GetDefaultMenuText, _win32_ICommDlgBrowser2_GetDefaultMenuText, shell.ICommDlgBrowser2_GetDefaultMenuText, shobjidl_core/ICommDlgBrowser2::GetDefaultMenuText
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICommDlgBrowser2.GetDefaultMenuText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICommDlgBrowser2::GetDefaultMenuText


## -description


Called by the Shell view to get the default shortcut menu text.


## -parameters




### -param ppshv

TBD


### -param pszText

Type: <b>WCHAR*</b>

A pointer to a buffer that is used by the Shell browser to return the default shortcut menu text.


### -param cchMax

Type: <b>int</b>

The size of the <i>pszText</i> buffer, in characters. It should be at least the maximum allowable path length (MAX_PATH) in size.


#### - pshv

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface of the hosted view.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if a new default shortcut menu text was returned in <i>pshv</i>. If S_FALSE is returned, use the normal default text. Otherwise, returns a standard COM error value.



