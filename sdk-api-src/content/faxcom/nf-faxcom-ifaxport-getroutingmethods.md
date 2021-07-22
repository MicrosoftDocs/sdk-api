---
UID: NF:faxcom.IFaxPort.GetRoutingMethods
title: IFaxPort::GetRoutingMethods (faxcom.h)
description: The IFaxPort::GetRoutingMethods interface method creates a FaxRoutingMethods object for the parent FaxPort object.
helpviewer_keywords: ["GetRoutingMethods","GetRoutingMethods method [Fax Service]","GetRoutingMethods method [Fax Service]","IFaxPort interface","IFaxPort interface [Fax Service]","GetRoutingMethods method","IFaxPort.GetRoutingMethods","IFaxPort::GetRoutingMethods","_mfax_ifaxport_getroutingmethods","fax._mfax_ifaxport_getroutingmethods","fax._mfax_ifaxport_mfax_ifaxport_getroutingmethods_cpp","faxcom/IFaxPort::GetRoutingMethods"]
old-location: fax\_mfax_ifaxport_mfax_ifaxport_getroutingmethods_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_619v.htm
ms.date: 12/05/2018
ms.keywords: GetRoutingMethods, GetRoutingMethods method [Fax Service], GetRoutingMethods method [Fax Service],IFaxPort interface, IFaxPort interface [Fax Service],GetRoutingMethods method, IFaxPort.GetRoutingMethods, IFaxPort::GetRoutingMethods, _mfax_ifaxport_getroutingmethods, fax._mfax_ifaxport_getroutingmethods, fax._mfax_ifaxport_mfax_ifaxport_getroutingmethods_cpp, faxcom/IFaxPort::GetRoutingMethods
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
 - IFaxPort::GetRoutingMethods
 - faxcom/IFaxPort::GetRoutingMethods
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
 - IFaxPort.GetRoutingMethods
---

# IFaxPort::GetRoutingMethods


## -description

The <b>IFaxPort::GetRoutingMethods</b> interface method creates a <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethods">FaxRoutingMethods</a> object for the parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The FaxRoutingMethods object allows enumeration of the fax routing methods associated with a fax port. Fax routing methods are defined by a fax routing extension DLL.

## -parameters

### -param retval [out]

Type: <b><a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>*</b>

Pointer to a <b>VARIANT</b> structure that receives an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethods">FaxRoutingMethods</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>IFaxPort::GetRoutingMethods</b> interface method retrieves an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethods">FaxRoutingMethods</a> object. This object is derived from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object specified by the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a> interface.

A fax client application can access the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethods">IFaxRoutingMethods</a> interface directly by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an interface pointer.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethods">IFaxRoutingMethods</a>