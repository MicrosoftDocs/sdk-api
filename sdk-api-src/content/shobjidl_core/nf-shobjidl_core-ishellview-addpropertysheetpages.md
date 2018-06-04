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

# IShellView::AddPropertySheetPages


## -description


Allows the view to add pages to the <b>Options</b> property sheet from the <b>View</b> menu.


## -parameters




### -param dwReserved [in]

Type: <b>DWORD</b>

Reserved.


### -param pfn




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
 

 

