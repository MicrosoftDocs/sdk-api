---
UID: NF:faxcom.IFaxRoutingMethods.get_Count
title: IFaxRoutingMethods::get_Count (faxcom.h)
description: The IFaxRoutingMethods::get_Count returns the number of fax routing methods associated with a FaxPort object.
helpviewer_keywords: ["IFaxRoutingMethods interface [Fax Service]","get_Count method","IFaxRoutingMethods.get_Count","IFaxRoutingMethods::get_Count","_mfax_ifaxroutingmethods_get_count","fax._mfax_ifaxroutingmethods_get_count","faxcom/IFaxRoutingMethods::get_Count","get_Count","get_Count method [Fax Service]","get_Count method [Fax Service]","IFaxRoutingMethods interface"]
old-location: fax\_mfax_ifaxroutingmethods_get_count.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0lis.htm
ms.date: 12/05/2018
ms.keywords: IFaxRoutingMethods interface [Fax Service],get_Count method, IFaxRoutingMethods.get_Count, IFaxRoutingMethods::get_Count, _mfax_ifaxroutingmethods_get_count, fax._mfax_ifaxroutingmethods_get_count, faxcom/IFaxRoutingMethods::get_Count, get_Count, get_Count method [Fax Service], get_Count method [Fax Service],IFaxRoutingMethods interface
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
 - IFaxRoutingMethods::get_Count
 - faxcom/IFaxRoutingMethods::get_Count
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
 - IFaxRoutingMethods.get_Count
---

# IFaxRoutingMethods::get_Count


## -description

The <b>IFaxRoutingMethods::get_Count</b> returns the number of fax routing methods associated with a <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object.

## -parameters

### -param pVal [out]

Type: <b>LONG*</b>

A pointer to a <b>LONG</b> that receives the number of routing methods associated with this fax port.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After calling the <b>IFaxRoutingMethods::get_Count</b> method, a fax client application can call the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxroutingmethods-get_item">IFaxRoutingMethods::get_Item</a> method to retrieve interface pointers to one or more <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> objects.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-getroutingmethods-vb">GetRoutingMethods</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethods">IFaxRoutingMethods</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxroutingmethods-get_item">IFaxRoutingMethods::get_Item</a>