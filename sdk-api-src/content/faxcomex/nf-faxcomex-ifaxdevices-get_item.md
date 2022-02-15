---
UID: NF:faxcomex.IFaxDevices.get_Item
title: IFaxDevices::get_Item (faxcomex.h)
description: The IFaxDevices::get_Item method returns a FaxDevice object from the FaxDevices collection, using its index.
helpviewer_keywords: ["IFaxDevices interface [Fax Service]","get_Item method","IFaxDevices.get_Item","IFaxDevices::get_Item","_mfax_faxdevices.item_cpp","fax._mfax_faxdevices_item_cpp","faxcomex/IFaxDevices::get_Item","get_Item","get_Item method [Fax Service]","get_Item method [Fax Service]","IFaxDevices interface"]
old-location: fax\_mfax_faxdevices_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5j8t_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDevices interface [Fax Service],get_Item method, IFaxDevices.get_Item, IFaxDevices::get_Item, _mfax_faxdevices.item_cpp, fax._mfax_faxdevices_item_cpp, faxcomex/IFaxDevices::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxDevices interface
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
 - IFaxDevices::get_Item
 - faxcomex/IFaxDevices::get_Item
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
 - IFaxDevices.get_Item
---

# IFaxDevices::get_Item


## -description

The <b>IFaxDevices::get_Item</b> method returns a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a> object from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevices">FaxDevices</a> collection, using its index.

## -parameters

### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies the index of the item to retrieve from the fax device collection. If this parameter is type VT_I2 or VT_I4, the parameter specifies the index of the item to retrieve from the collection. Valid values for the index are in the range from 1 to n, where n is the number of devices returned by a call to the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevices-count-vb">IFaxDevices::get_Count</a> method. If this parameter is type VT_BSTR, the parameter is a string containing the unique name of the fax device to retrieve. Other types are not supported.

### -param pFaxDevice [out]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevice">IFaxDevice</a>**</b>

Receives the address of a pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To retrieve an item from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevices">FaxDevices</a> collection using the device ID, call the <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdevices-get_itembyid">IFaxDevices::get_ItemById</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevices">IFaxDevices</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-configuring-a-fax-device">Visual Basic Example</a>