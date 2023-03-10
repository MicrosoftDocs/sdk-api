---
UID: NF:faxcomex.IFaxDeviceProviders.get_Item
title: IFaxDeviceProviders::get_Item (faxcomex.h)
description: The IFaxDeviceProviders::get_Item property returns a FaxDeviceProvider object from the FaxDeviceProviders collection.
helpviewer_keywords: ["IFaxDeviceProviders interface [Fax Service]","get_Item method","IFaxDeviceProviders.get_Item","IFaxDeviceProviders::get_Item","_mfax_faxdeviceproviders.item_cpp","fax._mfax_faxdeviceproviders_item_cpp","faxcomex/IFaxDeviceProviders::get_Item","get_Item","get_Item method [Fax Service]","get_Item method [Fax Service]","IFaxDeviceProviders interface"]
old-location: fax\_mfax_faxdeviceproviders_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_7fsd_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDeviceProviders interface [Fax Service],get_Item method, IFaxDeviceProviders.get_Item, IFaxDeviceProviders::get_Item, _mfax_faxdeviceproviders.item_cpp, fax._mfax_faxdeviceproviders_item_cpp, faxcomex/IFaxDeviceProviders::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxDeviceProviders interface
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
 - IFaxDeviceProviders::get_Item
 - faxcomex/IFaxDeviceProviders::get_Item
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
 - IFaxDeviceProviders.get_Item
---

# IFaxDeviceProviders::get_Item


## -description

The <b>IFaxDeviceProviders::get_Item</b> property returns a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider">FaxDeviceProvider</a> object from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceproviders">FaxDeviceProviders</a> collection.

## -parameters

### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies the item to retrieve from the collection.
                    
                    

If this parameter is type VT_I2 or VT_I4, the parameter specifies the index of the item to retrieve from the collection. The index is 1-based. If this parameter is type VT_BSTR, the parameter is the unique name that identifies the FSP to retrieve. Other types are not supported.

### -param pFaxDeviceProvider [out]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceprovider">IFaxDeviceProvider</a>**</b>

Address of a pointer to a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceprovider">IFaxDeviceProvider</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider">FaxDeviceProvider</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceprovider">IFaxDeviceProvider</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceproviders">IFaxDeviceProviders</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-fax-device-providers">Visual Basic Example</a>