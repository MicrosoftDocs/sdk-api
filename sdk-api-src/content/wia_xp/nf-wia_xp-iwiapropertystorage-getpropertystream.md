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

# IWiaPropertyStorage::GetPropertyStream


## -description


The <b>IWiaPropertyStorage::GetPropertyStream</b> method retrieves the property stream of an item.


## -parameters




### -param pCompatibilityId




### -param ppIStream [out]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>**</b>

Pointer to a stream that receives the item properties. For more information, see <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.


#### - pCompatibilityID [out]

Type: <b>GUID*</b>

Receives a unique identifier for a set of property values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications use this method to get a snapshot of the current properties of an item. These are subsequently restored by calling <a href="https://msdn.microsoft.com/44f25d8c-7f83-4c36-b582-abb6678ed78e">IWiaPropertyStorage::SetPropertyStream</a>.

Applications can use the <i>pCompatibilityID</i> parameter to check if a device supports a specific set of property values before attempting to write these values to the device.

When it is finished using the item's property stream, the application must release it.




## -see-also




<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/b80d22d4-8e36-484a-9dd1-f228e2236eaf">IWiaPropertyStorage</a>
 

 

