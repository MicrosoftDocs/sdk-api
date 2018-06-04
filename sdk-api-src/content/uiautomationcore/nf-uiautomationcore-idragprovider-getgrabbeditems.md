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

# IDragProvider::GetGrabbedItems


## -description


Retrieves the collection of elements that are being dragged as part of a drag operation.  


## -parameters




### -param pRetVal [out, retval, optional]

An array of VT_UNKNOWN pointers to the <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a> interfaces
				of the elements that are being dragged. This parameter is <b>NULL</b> if only a single item is being dragged. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the user is dragging multiple items, the items are represented by a single master element with an associated set of grabbed elements.  The master element raises the appropriate events, to avoid having a large set of duplicate events.  The client can call <b>GetGrabbedItems</b> to retrieve the full list of grabbed items.  The provider should allocate a <a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> of appropriate length and add the Component Object Model (COM) pointers of the elements that are part of the drag operation.  




## -see-also




<a href="https://msdn.microsoft.com/FAC4A56D-17BC-42E6-A03E-EE45D717DE37">IDragProvider</a>
 

 

