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

# MsiPreviewDialogA function


## -description


The 
<b>MsiPreviewDialog</b> function displays a dialog box as modeless and inactive.


## -parameters




### -param hPreview [in]

Handle to the preview.


### -param szDialogName [in]

Specifies the name of the dialog box to preview.


## -returns



This function returns UINT.




## -remarks



Supplying a null name in the 
<b>MsiPreviewDialog</b> function removes any current dialog box.




## -see-also




<a href="database_functions.htm">User Interface Functions</a>
 

 

