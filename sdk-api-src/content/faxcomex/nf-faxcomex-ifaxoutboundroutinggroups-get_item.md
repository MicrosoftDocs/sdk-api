---
UID: NF:faxcomex.IFaxOutboundRoutingGroups.get_Item
title: IFaxOutboundRoutingGroups::get_Item (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutboundRoutingGroups::get_Item method returns a IFaxOutboundRoutingGroup interface from the collection.
old-location: fax\_mfax_faxoutboundroutinggroups_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8l9p_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingGroups interface [Fax Service],get_Item method, IFaxOutboundRoutingGroups.get_Item, IFaxOutboundRoutingGroups::get_Item, _mfax_faxoutboundroutinggroups.item_cpp, fax._mfax_faxoutboundroutinggroups_item_cpp, faxcomex/IFaxOutboundRoutingGroups::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxOutboundRoutingGroups interface
ms.topic: method
f1_keywords: 
 - "faxcomex/IFaxOutboundRoutingGroups.get_Item"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutboundRoutingGroups::get_Item


## -description


The <b>IFaxOutboundRoutingGroups::get_Item</b> method returns a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroup">IFaxOutboundRoutingGroup</a> interface from the collection.


## -parameters




### -param vIndex [in]

Type: <b>VARIANT</b>


<a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">Variant</a> that specifies the item to retrieve from the collection. 




If this parameter is type VT_I2 or VT_I4, the parameter specifies the index of the item to retrieve from the collection. The index is 1-based. If this parameter is type VT_BSTR, the parameter is a unique name that identifies the outbound routing group to retrieve. Other types are not supported.



### -param pFaxOutboundRoutingGroup [out, retval]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroup">IFaxOutboundRoutingGroup</a>**</b>

An address of a pointer that receives the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroup">IFaxOutboundRoutingGroup</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To return the group consisting of all of the devices, set <i>vIndex</i> equal to the constant <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-bstrgroupname-alldevices">bstrGROUPNAME_ALLDEVICES</a>. 
		




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroups">IFaxOutboundRoutingGroups</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-managing-outbound-routing-groups">Visual Basic Example</a>
 

 

