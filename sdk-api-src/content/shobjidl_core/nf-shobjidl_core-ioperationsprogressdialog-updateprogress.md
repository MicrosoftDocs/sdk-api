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

# IOperationsProgressDialog::UpdateProgress


## -description


Updates the current progress dialog, as specified.


## -parameters




### -param ullPointsCurrent [in]

Type: <b>ULONGLONG</b>

Current points, used for showing progress in points.


### -param ullPointsTotal [in]

Type: <b>ULONGLONG</b>

Total points, used for showing progress in points.


### -param ullSizeCurrent [in]

Type: <b>ULONGLONG</b>

Current size in bytes, used for showing progress in bytes.


### -param ullSizeTotal [in]

Type: <b>ULONGLONG</b>

Total size in bytes, used for showing progress in bytes.


### -param ullItemsCurrent [in]

Type: <b>ULONGLONG</b>

Current items, used for showing progress in items.


### -param ullItemsTotal [in]

Type: <b>ULONGLONG</b>

Specifies total items, used for showing progress in items.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



