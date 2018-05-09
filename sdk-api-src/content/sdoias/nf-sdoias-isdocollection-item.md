---
UID: NF:sdoias.ISdoCollection.Item
title: ISdoCollection::Item
author: windows-driver-content
description: The Item method retrieves the specified item from the collection.
old-location: nps\SDO_isdocollection_item.htm
old-project: Nps
ms.assetid: 1c830e23-dc6f-49dd-83fe-8ddd39ac1bf6
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ISdoCollection interface [Network Policy Server],Item method, ISdoCollection.Item, ISdoCollection::Item, Item, Item method [Network Policy Server], Item method [Network Policy Server],ISdoCollection interface, _sdo_isdocollection_item, nps.SDO_isdocollection_item, sdo.isdocollection_item, sdoias/ISdoCollection::Item
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VENDORPROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Iassdo.dll
api_name:
-	ISdoCollection.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISdoCollection::Item


## -description


The 
<b>Item</b> method retrieves the specified item from the collection.


## -parameters




### -param Name [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>. Store the name of the object in a 
<a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> in this <b>VARIANT</b>.


### -param pItem [out]

Pointer to an interface pointer that receives the address of an 
<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface for the object.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the object is not found in the collection, the return value is <b>DISP_E_MEMBERNOTFOUND</b>.

Otherwise, if the method fails, the return value is one of the following error codes.




## -remarks



Neither of the parameters can be <b>NULL</b>.




## -see-also




<a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>



<a href="https://msdn.microsoft.com/9c7ee4d7-987f-45ae-810f-fc310955f36d">IASCOMMONPROPERTIES</a>



<a href="https://msdn.microsoft.com/26470906-1cba-41fc-96f3-078208ab3d51">ISdoCollection</a>



<a href="https://msdn.microsoft.com/df7cbff5-2d09-4031-8f41-3f4eea51598f">Retrieving an Object from a Collection</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>
 

 

