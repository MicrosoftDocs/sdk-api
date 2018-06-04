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

# MsiPreviewBillboardW function


## -description


The 
<b>MsiPreviewBillboard</b> function displays a billboard with the host control in the displayed dialog box.


## -parameters




### -param hPreview [in]

Handle to the preview.


### -param szControlName [in]

Specifies the name of the host control.


### -param szBillboard [in]

Specifies the name of the billboard to display.


## -returns



This function returns UINT.




## -remarks



Supplying a null billboard name in the 
<b>MsiPreviewBillboard</b> function removes any billboard displayed.




## -see-also




<a href="database_functions.htm">User Interface Functions</a>
 

 

