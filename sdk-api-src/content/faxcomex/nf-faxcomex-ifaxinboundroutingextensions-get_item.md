---
UID: NF:faxcomex.IFaxInboundRoutingExtensions.get_Item
title: IFaxInboundRoutingExtensions::get_Item
author: windows-sdk-content
description: The IFaxInboundRoutingExtensions::get_Item method returns a IFaxInboundRoutingExtension interface from the IFaxInboundRoutingExtensions collection.
old-location: fax\_mfax_faxinboundroutingextensions_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_9mwd_cpp.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxInboundRoutingExtensions interface [Fax Service],get_Item method, IFaxInboundRoutingExtensions.get_Item, IFaxInboundRoutingExtensions::get_Item, _mfax_faxinboundroutingextensions.item_cpp, fax._mfax_faxinboundroutingextensions_item_cpp, faxcomex/IFaxInboundRoutingExtensions::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxInboundRoutingExtensions interface
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
 - IFaxInboundRoutingExtensions.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxInboundRoutingExtensions::get_Item


## -description


The <b>IFaxInboundRoutingExtensions::get_Item</b> method returns a <a href="https://msdn.microsoft.com/e967c113-a4c0-4a83-949b-eb51fe41fb42">IFaxInboundRoutingExtension</a> interface from the <a href="https://msdn.microsoft.com/6daf0614-c0d4-42ba-96de-60f35a39aff1">IFaxInboundRoutingExtensions</a> collection.


## -parameters




### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies the item to retrieve from the collection. 

                    

If this parameter is type VT_I2 or VT_I4, the parameter specifies the index of the item to retrieve from the collection. The index is 1-based. If this parameter is type VT_BSTR, the parameter is a string containing the unique name of the fax routing extension to retrieve. Other types are not supported.


### -param pFaxInboundRoutingExtension

TBD




#### - ppFaxInboundRoutingExtension [out, retval]

Type: <b><a href="https://msdn.microsoft.com/e967c113-a4c0-4a83-949b-eb51fe41fb42">IFaxInboundRoutingExtension</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/e967c113-a4c0-4a83-949b-eb51fe41fb42">IFaxInboundRoutingExtension</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6daf0614-c0d4-42ba-96de-60f35a39aff1">IFaxInboundRoutingExtensions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693492(v=VS.85).aspx">Visual Basic Example</a>
 

 

