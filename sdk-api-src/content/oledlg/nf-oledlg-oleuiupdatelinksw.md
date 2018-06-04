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

# OleUIUpdateLinksW function


## -description


Updates all links in the link container and displays a dialog box that shows the progress of the updating process. The process is stopped if the user presses the <b>Stop</b> button or when all links are processed.


## -parameters




### -param lpOleUILinkCntr [in]

Pointer to the <a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a> interface on the link container.


### -param hwndParent [in]

Parent window of the dialog box.


### -param lpszTitle [in]

Pointer to the title of the dialog box.


### -param cLinks [in]

Total number of links.


## -returns



Returns <b>TRUE</b> if the links were successfully updated; otherwise, <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/136894a6-ddf6-4a47-80f5-997625362536">IOleUILinkContainer::GetLinkUpdateOptions</a>



<a href="https://msdn.microsoft.com/fccee32a-3a6f-4ef8-9ca7-c5b664ee03cf">IOleUILinkContainer::UpdateLink</a>
 

 

