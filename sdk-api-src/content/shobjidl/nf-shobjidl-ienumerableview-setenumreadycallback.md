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

# IEnumerableView::SetEnumReadyCallback


## -description


Sets a callback on the view that is notified when the initial view enumeration is complete.


## -parameters




### -param percb [in]

Type: <b><a href="https://msdn.microsoft.com/6c36e13d-9bd8-4ec1-980a-dc4ebd4dbcd9">IEnumReadyCallback</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/6c36e13d-9bd8-4ec1-980a-dc4ebd4dbcd9">IEnumReadyCallback</a> interface.


## -returns



Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.



