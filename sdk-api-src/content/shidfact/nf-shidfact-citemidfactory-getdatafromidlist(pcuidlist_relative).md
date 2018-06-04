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

# CItemIDFactory::GetDataFromIDList(PCUIDLIST_RELATIVE)


## -description


Gets a read only pointer to the client provided structure in the first ItemID in the IDList.


## -parameters




### -param pidl [in]

A PIDL containing the data.


#### - ppData [out]

When this method returns, contains the address of a read only pointer to a client provided structure.


## -returns



If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns <b>E_INVALIDARG</b>.




## -see-also




<a href="https://msdn.microsoft.com/8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7">CItemIDFactory</a>
 

 

