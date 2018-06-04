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

# IUICollectionChangedEvent::OnChanged


## -description


Called when an <a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a> changes.


## -parameters




### -param action [in]

Type: <b><a href="https://msdn.microsoft.com/8edb3772-04c6-45ac-8ccf-2b8ddd37db6d">UI_COLLECTIONCHANGE</a></b>


					The <a href="https://msdn.microsoft.com/library/windows/hardware/mt270124">action</a> performed on the 
					<a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a>.
				


### -param oldIndex [in]

Type: <b>UINT32</b>


					Index of the old item on remove or replace; otherwise <a href="https://msdn.microsoft.com/0524c712-c968-4a2c-955e-c92f21f2b1da">UI_COLLECTION_INVALIDINDEX</a>.
				


### -param oldItem [in]

Type: <b><a href="_com_iunknown">IUnknown</a>*</b>


					Pointer to the old item on remove or replace; otherwise <b>NULL</b>.
				


### -param newIndex [in]

Type: <b>UINT32</b>


					Index of the new item on insert, add, or replace; otherwise <a href="https://msdn.microsoft.com/0524c712-c968-4a2c-955e-c92f21f2b1da">UI_COLLECTION_INVALIDINDEX</a>.
				


### -param newItem [in]

Type: <b><a href="_com_iunknown">IUnknown</a>*</b>


					Pointer to the new item on insert, add, or replace; otherwise <b>NULL</b>.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




				The <b>IUICollectionChangedEvent::OnChanged</b> interface is implemented by the Ribbon host application 
				(the client connection sink) as a listener for collection changed 
				events that are fired by the Ribbon (the connectable object).
			




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=132598">Events in COM and Connectable Objects</a>



<a href="https://msdn.microsoft.com/1a462f4e-e75a-40cf-9c52-0bad0a645d57">Gallery Sample</a>



<a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a>



<a href="https://msdn.microsoft.com/f2342459-af53-4442-8280-27ad96e5868e">IUICollectionChangedEvent</a>
 

 

