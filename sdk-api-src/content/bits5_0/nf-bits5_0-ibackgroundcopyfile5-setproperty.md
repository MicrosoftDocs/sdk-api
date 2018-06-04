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

# IBackgroundCopyFile5::SetProperty


## -description


Sets a generic property of a BITS file transfer.


## -parameters




### -param PropertyId [in]

Specifies the property to be set.


### -param PropertyValue






#### - ProertyValue [out]

A pointer to a union that specifies the value to be set. The union member appropriate for the property ID is used.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/548b507a-4874-4ccf-829e-13e1ca6cc958">IBackgroundCopyFile5</a>



<a href="https://msdn.microsoft.com/7afe4d11-f611-40ea-be94-7825f95576de">IBackgroundCopyFile5.GetProperty</a>
 

 

