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

# IFaxOutboundRoutingGroups::get_Item


## -description


The <b>IFaxOutboundRoutingGroups::get_Item</b> method returns a <a href="https://msdn.microsoft.com/147fbebd-0000-4a24-b9cf-da4132b46edf">IFaxOutboundRoutingGroup</a> interface from the collection.


## -parameters




### -param vIndex [in]

Type: <b>VARIANT</b>


<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">Variant</a> that specifies the item to retrieve from the collection. 




If this parameter is type VT_I2 or VT_I4, the parameter specifies the index of the item to retrieve from the collection. The index is 1-based. If this parameter is type VT_BSTR, the parameter is a unique name that identifies the outbound routing group to retrieve. Other types are not supported.



### -param pFaxOutboundRoutingGroup [out, retval]

Type: <b><a href="https://msdn.microsoft.com/147fbebd-0000-4a24-b9cf-da4132b46edf">IFaxOutboundRoutingGroup</a>**</b>

An address of a pointer that receives the <a href="https://msdn.microsoft.com/147fbebd-0000-4a24-b9cf-da4132b46edf">IFaxOutboundRoutingGroup</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




		To return the group consisting of all of the devices, set <i>vIndex</i> equal to the constant <a href="https://msdn.microsoft.com/a8a89fcb-2cd6-4923-b26e-7191328c405f">bstrGROUPNAME_ALLDEVICES</a>. 
		




## -see-also




<a href="https://msdn.microsoft.com/cf36787b-cc8e-48a8-b81d-5406cbc4bcc8">IFaxOutboundRoutingGroups</a>



<a href="https://msdn.microsoft.com/5a05df3b-c56b-4dfc-a0ee-7f1c2861e9ae">Visual Basic Example</a>
 

 

