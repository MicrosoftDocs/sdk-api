---
UID: NF:faxcomex.IFaxDeviceIds.get_Item
title: IFaxDeviceIds::get_Item (faxcomex.h)
description: The IFaxDeviceIds::get_Item method represents a device ID from the FaxDeviceIds collection.
helpviewer_keywords: ["IFaxDeviceIds interface [Fax Service]","get_Item method","IFaxDeviceIds.get_Item","IFaxDeviceIds::get_Item","_mfax_faxdeviceids.item_cpp","fax._mfax_faxdeviceids_item_cpp","faxcomex/IFaxDeviceIds::get_Item","get_Item","get_Item method [Fax Service]","get_Item method [Fax Service]","IFaxDeviceIds interface"]
old-location: fax\_mfax_faxdeviceids_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0xt9_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDeviceIds interface [Fax Service],get_Item method, IFaxDeviceIds.get_Item, IFaxDeviceIds::get_Item, _mfax_faxdeviceids.item_cpp, fax._mfax_faxdeviceids_item_cpp, faxcomex/IFaxDeviceIds::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxDeviceIds interface
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
 - IFaxDeviceIds::get_Item
 - faxcomex/IFaxDeviceIds::get_Item
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
 - IFaxDeviceIds.get_Item
---

# IFaxDeviceIds::get_Item


## -description

The <b>IFaxDeviceIds::get_Item</b> method represents a device ID from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection.

## -parameters

### -param lIndex [in]

Type: <b>long</b>

A value specifying the item to retrieve from the collection. Valid values for this parameter are in the range from 1 to n, where n is the number of devices returned by a call to the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids-count-vb">IFaxDeviceIds::get_Count</a> method.

### -param plDeviceId [out, retval]

Type: <b>long*</b>

Pointer to a value that receives the item requested.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceids">IFaxDeviceIds</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outbound-routing-groups">Visual Basic Example</a>