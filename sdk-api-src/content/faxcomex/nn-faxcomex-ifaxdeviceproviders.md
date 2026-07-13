---
UID: NN:faxcomex.IFaxDeviceProviders
title: IFaxDeviceProviders (faxcomex.h)
description: The IFaxDeviceProviders interface defines a configuration collection which contains the fax device providers on a connected fax server.
helpviewer_keywords: ["IFaxDeviceProviders","IFaxDeviceProviders interface [Fax Service]","IFaxDeviceProviders interface [Fax Service]","described","_mfax_faxdeviceproviders_cpp","fax._mfax_faxdeviceproviders_cpp","faxcomex/IFaxDeviceProviders"]
old-location: fax\_mfax_faxdeviceproviders_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_7vxv_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDeviceProviders, IFaxDeviceProviders interface [Fax Service], IFaxDeviceProviders interface [Fax Service],described, _mfax_faxdeviceproviders_cpp, fax._mfax_faxdeviceproviders_cpp, faxcomex/IFaxDeviceProviders
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
 - IFaxDeviceProviders
 - faxcomex/IFaxDeviceProviders
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
 - IFaxDeviceProviders
---

# IFaxDeviceProviders interface


## -description

The <b>IFaxDeviceProviders</b> interface defines a configuration collection which contains the fax device providers on a connected fax server. This collection is used by a fax client application to retrieve information about the fax service providers (FSPs) registered with the fax service, represented by <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider">FaxDeviceProvider</a> objects.

## -inheritance

The <b>IFaxDeviceProviders</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxDeviceProviders</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxDeviceProviders</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceproviders">FaxDeviceProviders</a> object.
