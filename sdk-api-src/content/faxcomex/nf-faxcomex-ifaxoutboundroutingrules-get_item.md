---
UID: NF:faxcomex.IFaxOutboundRoutingRules.get_Item
title: IFaxOutboundRoutingRules::get_Item
author: windows-sdk-content
description: The IFaxOutboundRoutingRules::get_Item method returns a IFaxOutboundRoutingRule interface from the IFaxOutboundRoutingRules interface using the routing rule's index.
old-location: fax\_mfax_faxoutboundroutingrules_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_73xp_cpp.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxOutboundRoutingRules interface [Fax Service],get_Item method, IFaxOutboundRoutingRules.get_Item, IFaxOutboundRoutingRules::get_Item, _mfax_faxoutboundroutingrules.item_cpp, fax._mfax_faxoutboundroutingrules_item_cpp, faxcomex/IFaxOutboundRoutingRules::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxOutboundRoutingRules interface
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
 - IFaxOutboundRoutingRules.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxOutboundRoutingRules.get_Item
: 
---

# IFaxOutboundRoutingRules::get_Item


## -description


The <b>IFaxOutboundRoutingRules::get_Item</b> method returns a <a href="https://msdn.microsoft.com/29b577f6-6aeb-43fd-8a0f-657ef1c16999">IFaxOutboundRoutingRule</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/ms689527(v=VS.85).aspx">IFaxOutboundRoutingRules</a> interface using the routing rule's index.


## -parameters




### -param lIndex [in]

Type: <b>long</b>

A <b>long</b> value that specifies the outbound routing rule to retrieve from the collection. Valid values for this parameter are in the range from 1 to n, where n is the number of items returned by a call to the <a href="https://msdn.microsoft.com/3add9157-b82a-4046-ad20-f6a29f92257e">IFaxOutboundRoutingRules::get_Count</a> method.


### -param pFaxOutboundRoutingRule [out, retval]

Type: <b><a href="https://msdn.microsoft.com/29b577f6-6aeb-43fd-8a0f-657ef1c16999">IFaxOutboundRoutingRule</a>**</b>

An address of a pointer that receives the <a href="https://msdn.microsoft.com/29b577f6-6aeb-43fd-8a0f-657ef1c16999">IFaxOutboundRoutingRule</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms689527(v=VS.85).aspx">IFaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693486(v=VS.85).aspx">Visual Basic Example</a>
 

 

