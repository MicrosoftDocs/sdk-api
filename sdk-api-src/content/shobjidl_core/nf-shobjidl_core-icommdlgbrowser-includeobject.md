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
 

 

