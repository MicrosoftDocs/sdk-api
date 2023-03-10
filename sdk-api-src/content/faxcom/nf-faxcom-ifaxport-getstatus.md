---
UID: NF:faxcom.IFaxPort.GetStatus
title: IFaxPort::GetStatus (faxcom.h)
description: The IFaxPort::GetStatus method creates a FaxStatus object for the parent FaxPort object. The FaxStatus object contains the current status of a fax port.
helpviewer_keywords: ["GetStatus","GetStatus method [Fax Service]","GetStatus method [Fax Service]","IFaxPort interface","IFaxPort interface [Fax Service]","GetStatus method","IFaxPort.GetStatus","IFaxPort::GetStatus","_mfax_ifaxport_getstatus","fax._mfax_ifaxport_getstatus","fax._mfax_ifaxport_mfax_ifaxport_getstatus_cpp","faxcom/IFaxPort::GetStatus"]
old-location: fax\_mfax_ifaxport_mfax_ifaxport_getstatus_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8lo3.htm
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Fax Service], GetStatus method [Fax Service],IFaxPort interface, IFaxPort interface [Fax Service],GetStatus method, IFaxPort.GetStatus, IFaxPort::GetStatus, _mfax_ifaxport_getstatus, fax._mfax_ifaxport_getstatus, fax._mfax_ifaxport_mfax_ifaxport_getstatus_cpp, faxcom/IFaxPort::GetStatus
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
 - IFaxPort::GetStatus
 - faxcom/IFaxPort::GetStatus
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
 - IFaxPort.GetStatus
---

# IFaxPort::GetStatus


## -description

The <b>IFaxPort::GetStatus</b> method creates a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object for the parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The FaxStatus object contains the current status of a fax port.

## -parameters

### -param retval [out]

Type: <b><a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>*</b>

Pointer to a <b>VARIANT</b> structure that receives an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>IFaxPort::GetStatus</b> method retrieves an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object. A fax client application can also access the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a> interface directly by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxStatus</b> interface pointer.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>