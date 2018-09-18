---
UID: NF:shobjidl_core.IShellView.AddPropertySheetPages
title: IShellView::AddPropertySheetPages
author: windows-sdk-content
description: Allows the view to add pages to the Options property sheet from the View menu.
old-location: shell\IShellView_AddPropertySheetPages.htm
tech.root: shell
ms.assetid: 6f05ddf7-190e-41f5-b24a-d18112b34600
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: AddPropertySheetPages, AddPropertySheetPages method [Windows Shell], AddPropertySheetPages method [Windows Shell],IShellView interface, IShellView interface [Windows Shell],AddPropertySheetPages method, IShellView.AddPropertySheetPages, IShellView::AddPropertySheetPages, _win32_IShellView_AddPropertySheetPages, shell.IShellView_AddPropertySheetPages, shobjidl_core/IShellView::AddPropertySheetPages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IShellView.AddPropertySheetPages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellView::AddPropertySheetPages


## -description


Allows the view to add pages to the <b>Options</b> property sheet from the <b>View</b> menu.


## -parameters




### -param dwReserved [in]

Type: <b>DWORD</b>

Reserved.


### -param pfn

TBD


### -param lparam [in]

Type: <b>LPARAM</b>

A value that must be passed as the callback function's <i>lparam</i> parameter.


#### - lpfn [in]

Type: <b>LPFNADDPROPSHEETPAGE</b>

The address of the callback function used to add the pages.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Windows Explorer calls this method when it is opening the <b>Options</b> property sheet from the <b>View</b> menu. Views can add pages by creating them and calling the callback function with the page handles.




## -see-also




<a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>
 

 

