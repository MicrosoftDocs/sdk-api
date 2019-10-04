---
UID: NF:shobjidl_core.IShellBrowser.QueryActiveShellView
title: IShellBrowser::QueryActiveShellView (shobjidl_core.h)
author: windows-sdk-content
description: Retrieves the currently active (displayed) Shell view object.
old-location: shell\IShellBrowser_QueryActiveShellView.htm
tech.root: shell
ms.assetid: d03e41dc-72dc-4f34-ae5b-b5ef8b2f146d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellBrowser interface [Windows Shell],QueryActiveShellView method, IShellBrowser.QueryActiveShellView, IShellBrowser::QueryActiveShellView, QueryActiveShellView, QueryActiveShellView method [Windows Shell], QueryActiveShellView method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_QueryActiveShellView, shell.IShellBrowser_QueryActiveShellView, shobjidl_core/IShellBrowser::QueryActiveShellView
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IShellBrowser.QueryActiveShellView"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellBrowser.QueryActiveShellView
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellBrowser::QueryActiveShellView


## -description


Retrieves the currently active (displayed) Shell view object.


## -parameters




### -param ppshv

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>**</b>

The address of the pointer to the currently active Shell view object.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.




## -remarks



<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
Because the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a> interface can host several Shell views simultaneously, this method provides an easy way to determine the active Shell view object.



