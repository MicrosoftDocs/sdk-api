---
UID: NF:faxcom.IFaxPorts.get_Item
title: IFaxPorts::get_Item (faxcom.h)
description: The IFaxPorts::get_Item method creates a FaxPort object for a specified fax port. The object allows enumeration of port configuration information for a specific connection to a fax server.
helpviewer_keywords: ["IFaxPorts interface [Fax Service]","get_Item method","IFaxPorts.get_Item","IFaxPorts::get_Item","_mfax_ifaxports_get_item","fax._mfax_ifaxports_get_item","faxcom/IFaxPorts::get_Item","get_Item","get_Item method [Fax Service]","get_Item method [Fax Service]","IFaxPorts interface"]
old-location: fax\_mfax_ifaxports_get_item.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0i0d.htm
ms.date: 12/05/2018
ms.keywords: IFaxPorts interface [Fax Service],get_Item method, IFaxPorts.get_Item, IFaxPorts::get_Item, _mfax_ifaxports_get_item, fax._mfax_ifaxports_get_item, faxcom/IFaxPorts::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxPorts interface
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxPorts::get_Item
 - faxcom/IFaxPorts::get_Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxPorts.get_Item
---

# IFaxPorts::get_Item


## -description

The <b>IFaxPorts::get_Item</b> method creates a <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object for a specified fax port. The object allows enumeration of port configuration information for a specific connection to a fax server.

## -parameters

### -param Index [in]

Type: <b>LONG</b>

Specifies a <b>LONG</b> variable that indicates the fax port to retrieve. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of fax ports returned by a call to the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_count">IFaxPorts::get_Count</a> method.

### -param pVal [out]

Type: <b>VARIANT*</b>

Receives a pointer to a <b>VARIANT</b> structure that receives an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A fax client application can also access the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a> interface directly by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxPort</b> interface pointer.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getports-vb">GetPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_count">IFaxPorts::get_Count</a>