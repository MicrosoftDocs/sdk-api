---
UID: NF:faxcomex.IFaxDevice.UseRoutingMethod
title: IFaxDevice::UseRoutingMethod (faxcomex.h)
description: The IFaxDevice::UseRoutingMethod method adds an inbound fax routing method to or removes a fax routing method (FaxInboundRoutingMethod) from the list of routing methods associated with the fax device.
helpviewer_keywords: ["IFaxDevice interface [Fax Service]","UseRoutingMethod method","IFaxDevice.UseRoutingMethod","IFaxDevice::UseRoutingMethod","UseRoutingMethod","UseRoutingMethod method [Fax Service]","UseRoutingMethod method [Fax Service]","IFaxDevice interface","_mfax_faxdevice.useroutingmethod","fax._mfax_faxdevice_cpp_mfax_faxdevice_useroutingmethod_cpp","fax._mfax_faxdevice_useroutingmethod","faxcomex/IFaxDevice::UseRoutingMethod"]
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_useroutingmethod_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_2m90.htm
ms.date: 12/05/2018
ms.keywords: IFaxDevice interface [Fax Service],UseRoutingMethod method, IFaxDevice.UseRoutingMethod, IFaxDevice::UseRoutingMethod, UseRoutingMethod, UseRoutingMethod method [Fax Service], UseRoutingMethod method [Fax Service],IFaxDevice interface, _mfax_faxdevice.useroutingmethod, fax._mfax_faxdevice_cpp_mfax_faxdevice_useroutingmethod_cpp, fax._mfax_faxdevice_useroutingmethod, faxcomex/IFaxDevice::UseRoutingMethod
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
 - IFaxDevice::UseRoutingMethod
 - faxcomex/IFaxDevice::UseRoutingMethod
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
 - IFaxDevice.UseRoutingMethod
 - IFaxDevice.UseRoutingMethod
---

# IFaxDevice::UseRoutingMethod


## -description

The <b>IFaxDevice::UseRoutingMethod</b> method adds an inbound fax routing method to or removes a fax routing method (<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod">FaxInboundRoutingMethod</a>) from the list of routing methods associated with the fax device.

## -parameters

### -param bstrMethodGUID [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that uniquely identifies the fax routing method to add or remove.

### -param bUse [in]

Type: <b>VARIANT_BOOL</b>

Specifies a Boolean value. If this parameter is equal to <b>TRUE</b>, the method adds the fax routing method to the list of inbound methods associated with the fax device. If you set this parameter to <b>FALSE</b>, the method removes the routing method from the list.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevice">IFaxDevice</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-fax-device-collection">Visual Basic Example</a>