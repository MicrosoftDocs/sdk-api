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

# IFolderActionCollection::Remove


## -description


Removes a folder action from the collection based on the specified index.


## -parameters




### -param Index [in]

The zero-based index of the folder action to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.


## -returns



Returns S_OK if successful.




## -remarks



If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="https://msdn.microsoft.com/a3942d5f-9ec4-4461-84f9-f2fae3971e23">IFolderAction</a> interface to be removed.




## -see-also




<a href="https://msdn.microsoft.com/9b0ab26f-7e91-4d7a-9fd7-73332601dd7b">IFolderActionCollection</a>



<a href="https://msdn.microsoft.com/39597249-29d5-44a0-9954-01b9b6a62977">IFolderActionCollection::Add</a>



<a href="https://msdn.microsoft.com/357934fa-9213-466e-8104-eb9b265a98d3">IFolderActionCollection::Clear</a>
 

 

