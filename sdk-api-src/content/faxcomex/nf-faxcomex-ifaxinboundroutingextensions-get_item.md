---
UID: NF:faxcomex.IFaxInboundRoutingExtensions.get_Item
title: IFaxInboundRoutingExtensions::get_Item (faxcomex.h)
description: The IFaxInboundRoutingExtensions::get_Item method returns a IFaxInboundRoutingExtension interface from the IFaxInboundRoutingExtensions collection.
helpviewer_keywords: ["IFaxInboundRoutingExtensions interface [Fax Service]","get_Item method","IFaxInboundRoutingExtensions.get_Item","IFaxInboundRoutingExtensions::get_Item","_mfax_faxinboundroutingextensions.item_cpp","fax._mfax_faxinboundroutingextensions_item_cpp","faxcomex/IFaxInboundRoutingExtensions::get_Item","get_Item","get_Item method [Fax Service]","get_Item method [Fax Service]","IFaxInboundRoutingExtensions interface"]
old-location: fax\_mfax_faxinboundroutingextensions_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_9mwd_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxInboundRoutingExtensions interface [Fax Service],get_Item method, IFaxInboundRoutingExtensions.get_Item, IFaxInboundRoutingExtensions::get_Item, _mfax_faxinboundroutingextensions.item_cpp, fax._mfax_faxinboundroutingextensions_item_cpp, faxcomex/IFaxInboundRoutingExtensions::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxInboundRoutingExtensions interface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxInboundRoutingExtensions::get_Item
 - faxcomex/IFaxInboundRoutingExtensions::get_Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxInboundRoutingExtensions.get_Item
---

# IFaxInboundRoutingExtensions::get_Item


## -description

The <b>IFaxInboundRoutingExtensions::get_Item</b> method returns a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingextension">IFaxInboundRoutingExtension</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingextensions">IFaxInboundRoutingExtensions</a> collection.

## -parameters

### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies the item to retrieve from the collection. 

                    

If this parameter is type VT_I2 or VT_I4, the parameter specifies the index of the item to retrieve from the collection. The index is 1-based. If this parameter is type VT_BSTR, the parameter is a string containing the unique name of the fax routing extension to retrieve. Other types are not supported.

### -param pFaxInboundRoutingExtension [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingextension">IFaxInboundRoutingExtension</a>**</b>

Address of a pointer to an <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingextension">IFaxInboundRoutingExtension</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingextensions">IFaxInboundRoutingExtensions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-routing-extensions-and-routing-methods">Visual Basic Example</a>