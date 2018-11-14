---
UID: NF:shobjidl_core.ICommDlgBrowser.IncludeObject
title: ICommDlgBrowser::IncludeObject
author: windows-sdk-content
description: Allows the common dialog box to filter objects that the view displays.
old-location: shell\ICommDlgBrowser_IncludeObject.htm
tech.root: shell
ms.assetid: f483dda2-5384-42b5-97ca-c7c6793d19a7
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICommDlgBrowser interface [Windows Shell],IncludeObject method, ICommDlgBrowser.IncludeObject, ICommDlgBrowser::IncludeObject, IncludeObject, IncludeObject method [Windows Shell], IncludeObject method [Windows Shell],ICommDlgBrowser interface, _win32_ICommDlgBrowser_IncludeObject, shell.ICommDlgBrowser_IncludeObject, shobjidl_core/ICommDlgBrowser::IncludeObject
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
 - ICommDlgBrowser.IncludeObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- ICommDlgBrowser.IncludeObject
: 
---

# ICommDlgBrowser::IncludeObject


## -description


Allows the common dialog box to filter objects that the view displays.


## -parameters




### -param ppshv

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the view's <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface.


### -param pidl

Type: <b>LPCITEMIDLIST</b>

A PIDL, relative to the folder, that identifies the object.


## -returns



Type: <b>HRESULT</b>

The browser should return S_OK to include the object in the view, or S_FALSE to hide it.




## -remarks



This method is called by the <a href="https://msdn.microsoft.com/b6f139d3-c54c-4350-9d8b-cd534909a488">IEnumIDList</a> implementation when hosted in file dialog boxes. The enumerator calls this method to let the common dialog box filter out objects that should not be displayed. Typically, the file dialog boxes will get the display text of the item, and filter by the extension.

<h3><a id="Note_to_Calling_Applications"></a><a id="note_to_calling_applications"></a><a id="NOTE_TO_CALLING_APPLICATIONS"></a>Note to Calling Applications</h3>
Call this method before returning an object in the Shell folder's IDLIST enumerator.

When dealing with data sources that have many items, such as libraries and searches, the callback to this method results in poor performance. To avoid that situation, implement <a href="https://msdn.microsoft.com/cb22504c-9f76-44c4-b81d-fc15d1b95143">GetViewFlags</a> and return CDB2GVF_NOINCLUDEITEM. Doing so enables the view to skip calling <b>ICommDlgBrowser::IncludeObject</b>, thereby improving performance.




## -see-also




<a href="https://msdn.microsoft.com/A7558455-06C4-48d1-8F85-B0FB682B52BB">Explorer Browser Search Sample</a>



<a href="https://msdn.microsoft.com/bf89ac6e-6c2e-4944-885c-9ab62f58fe71">ICommDlgBrowser</a>
 

 

