---
UID: NF:faxcom.IFaxRoutingMethods.get_Item
title: IFaxRoutingMethods::get_Item (faxcom.h)
description: The IFaxRoutingMethods::get_Item method creates a FaxRoutingMethod object for a specified fax routing method. The object allows enumeration of fax routing information for a specified FaxPort object.
helpviewer_keywords: ["IFaxRoutingMethods interface [Fax Service]","get_Item method","IFaxRoutingMethods.get_Item","IFaxRoutingMethods::get_Item","_mfax_ifaxroutingmethods_get_item","fax._mfax_ifaxroutingmethods_get_item","faxcom/IFaxRoutingMethods::get_Item","get_Item","get_Item method [Fax Service]","get_Item method [Fax Service]","IFaxRoutingMethods interface"]
old-location: fax\_mfax_ifaxroutingmethods_get_item.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7kq5.htm
ms.date: 12/05/2018
ms.keywords: IFaxRoutingMethods interface [Fax Service],get_Item method, IFaxRoutingMethods.get_Item, IFaxRoutingMethods::get_Item, _mfax_ifaxroutingmethods_get_item, fax._mfax_ifaxroutingmethods_get_item, faxcom/IFaxRoutingMethods::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxRoutingMethods interface
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
 - IFaxRoutingMethods::get_Item
 - faxcom/IFaxRoutingMethods::get_Item
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
 - IFaxRoutingMethods.get_Item
---

# IFaxRoutingMethods::get_Item


## -description

The <b>IFaxRoutingMethods::get_Item</b> method creates a <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> object for a specified fax routing method. The object allows enumeration of fax routing information for a specified <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object.

## -parameters

### -param Index [in]

Type: <b>LONG</b>

Specifies a <b>LONG</b> variable that indicates the fax routing method to retrieve. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of fax routing methods returned by a call to the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxroutingmethods-get_count">IFaxRoutingMethods::get_Count</a> method.

### -param pVal [out]

Type: <b>VARIANT*</b>

Receives a pointer to a <b>VARIANT</b> structure that receives an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A fax client application can also access the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a> interface directly by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxRoutingMethod</b> interface pointer.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-getroutingmethods-vb">GetRoutingMethods</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethods">IFaxRoutingMethods</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxroutingmethods-get_count">IFaxRoutingMethods::get_Count</a>