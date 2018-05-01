---
UID: NF:faxcomex.IFaxInboundRoutingMethods.get_Item
title: IFaxInboundRoutingMethods::get_Item method
author: windows-driver-content
description: The IFaxInboundRoutingMethods::get_Item method returns a IFaxInboundRoutingMethod object from the IFaxInboundRoutingMethods collection.
old-location: fax\_mfax_faxinboundroutingmethods_item_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6m5p_cpp.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxInboundRoutingMethods, IFaxInboundRoutingMethods interface [Fax Service], get_Item method, IFaxInboundRoutingMethods::get_Item, _mfax_faxinboundroutingmethods.item_cpp, fax._mfax_faxinboundroutingmethods_item_cpp, faxcomex/IFaxInboundRoutingMethods::get_Item, get_Item method [Fax Service], get_Item method [Fax Service], IFaxInboundRoutingMethods interface, get_Item,IFaxInboundRoutingMethods.get_Item
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxInboundRoutingMethods.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxInboundRoutingMethods::get_Item method


## -description


The <b>IFaxInboundRoutingMethods::get_Item</b> method returns a <a href="https://msdn.microsoft.com/ca33c439-24e7-4b85-8e29-a0a0176f0ae2">IFaxInboundRoutingMethod</a> object from the <a href="https://msdn.microsoft.com/5a19c7d9-f602-4271-a772-fdc61b73024f">IFaxInboundRoutingMethods</a> collection.


## -parameters




### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies the item to retrieve from the collection. 

                    

If this parameter is type VT_I2 or VT_I4, the parameter specifies the index of the item to retrieve from the collection. The index is 1-based. If this parameter is type VT_BSTR, the parameter is a GUID that identifies the fax routing method to retrieve. Other types are not supported.


### -param pFaxInboundRoutingMethod [out, retval]

Type: <b><a href="https://msdn.microsoft.com/ca33c439-24e7-4b85-8e29-a0a0176f0ae2">IFaxInboundRoutingMethod</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/ca33c439-24e7-4b85-8e29-a0a0176f0ae2">IFaxInboundRoutingMethod</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5a19c7d9-f602-4271-a772-fdc61b73024f">IFaxInboundRoutingMethods</a>



<a href="https://msdn.microsoft.com/cef24608-cab1-4090-aa94-3a1b76733e98">Visual Basic Example</a>
 

 

