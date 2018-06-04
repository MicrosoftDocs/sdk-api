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

# IBrowserService::IsControlWindowShown


## -description


Deprecated. Retrieves a value that indicates whether a specified frame control is currently visible.


## -parameters




### -param id [in]

Type: <b>UINT</b>

The frame control to check.

<div class="alert"><b>Note</b>  These frame controls may not be supported in future versions of Windows.</div>
<div> </div>


#### FCW_STATUS (0x0001)

The browser's status bar.



#### FCW_TOOLBAR (0x0002)

The browser's toolbar.



#### FCW_TREE (0x0003)

The browser's tree view.



#### FCW_INTERNETBAR (0x0006)

The browser's Media Bar.



#### FCW_PROGRESS (0x0008)

The browser's progress bar.


### -param pfShown [out]

Type: <b>BOOL*</b>

A value of type <b>BOOL</b> that indicates whether the specified frame control is visible.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



