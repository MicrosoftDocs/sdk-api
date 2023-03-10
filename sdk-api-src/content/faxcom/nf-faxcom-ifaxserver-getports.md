---
UID: NF:faxcom.IFaxServer.GetPorts
title: IFaxServer::GetPorts (faxcom.h)
description: The GetPorts method creates and initializes a FaxPorts object for a specified FaxServer object. The FaxPorts object allows enumeration of fax port configuration information for the connected fax server.
helpviewer_keywords: ["GetPorts","GetPorts method [Fax Service]","GetPorts method [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","GetPorts method","IFaxServer.GetPorts","IFaxServer::GetPorts","_mfax_ifaxserver_getports","fax._mfax_ifaxserver_client_mfax_ifaxserver_getports_cpp","fax._mfax_ifaxserver_getports","faxcom/IFaxServer::GetPorts"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_getports_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9apf.htm
ms.date: 12/05/2018
ms.keywords: GetPorts, GetPorts method [Fax Service], GetPorts method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],GetPorts method, IFaxServer.GetPorts, IFaxServer::GetPorts, _mfax_ifaxserver_getports, fax._mfax_ifaxserver_client_mfax_ifaxserver_getports_cpp, fax._mfax_ifaxserver_getports, faxcom/IFaxServer::GetPorts
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
 - IFaxServer::GetPorts
 - faxcom/IFaxServer::GetPorts
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
 - IFaxServer.GetPorts
 - IFaxServer.GetPorts
---

## -description

The <b>GetPorts</b> method creates and initializes a <a href="/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a> object for a specified <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The FaxPorts object allows enumeration of fax port configuration information for the connected fax server.

## -parameters

### -param retval [out]

Type: <b>VARIANT*</b>

Pointer to a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure that receives an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxports-object-visual-basic-">FaxPorts</a> object. The method returns a pdispVal member with a VT_DISPATCH data type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>IFaxServer::GetPorts</b> method retrieves an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a> object. A fax client application can also access the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a> interface directly by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an interface pointer.

A fax client application should not call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a> interface pointer because it will not be instantiated correctly.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>



<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>