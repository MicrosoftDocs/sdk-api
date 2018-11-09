---
UID: NF:faxcomex.IFaxOutboundRoutingGroups.get_Item
title: IFaxOutboundRoutingGroups::get_Item
author: windows-sdk-content
description: The IFaxOutboundRoutingGroups::get_Item method returns a IFaxOutboundRoutingGroup interface from the collection.
old-location: fax\_mfax_faxoutboundroutinggroups_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8l9p_cpp.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxOutboundRoutingGroups interface [Fax Service],get_Item method, IFaxOutboundRoutingGroups.get_Item, IFaxOutboundRoutingGroups::get_Item, _mfax_faxoutboundroutinggroups.item_cpp, fax._mfax_faxoutboundroutinggroups_item_cpp, faxcomex/IFaxOutboundRoutingGroups::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxOutboundRoutingGroups interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutboundRoutingGroups.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutboundRoutingGroups::get_Item


## -description


The <b>IFaxOutboundRoutingGroups::get_Item</b> method returns a <a href="https://msdn.microsoft.com/147fbebd-0000-4a24-b9cf-da4132b46edf">IFaxOutboundRoutingGroup</a> interface from the collection.


## -parameters




### -param vIndex [in]

Type: <b>VARIANT</b>


<a href="e305240e-9e11-4006-98cc-26f4932d2118">Variant</a> that specifies the item to retrieve from the collection. 




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
 

 

