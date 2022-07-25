---
UID: NN:faxcomex.IFaxDevice
title: IFaxDevice (faxcomex.h)
description: The IFaxDevice interface defines a configuration object used by a fax client application to retrieve and set fax device information, and to add and remove fax routing methods associated with a fax device.
helpviewer_keywords: ["IFaxDevice","IFaxDevice interface [Fax Service]","IFaxDevice interface [Fax Service]","described","_mfax_faxdevice_cpp","fax._mfax_faxdevice_cpp","faxcomex/IFaxDevice"]
old-location: fax\_mfax_faxdevice_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5nad_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDevice, IFaxDevice interface [Fax Service], IFaxDevice interface [Fax Service],described, _mfax_faxdevice_cpp, fax._mfax_faxdevice_cpp, faxcomex/IFaxDevice
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
 - IFaxDevice
 - faxcomex/IFaxDevice
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
 - IFaxDevice
---

# IFaxDevice interface


## -description

The <b>IFaxDevice</b> interface defines a configuration object used by a fax client application to retrieve and set fax device information, and to add and remove fax routing methods associated with a fax device. The object also includes methods to retrieve and set extension configuration properties stored at the device level. The object defined by the <b>IFaxDevice</b> interface represents a single device associated with a fax server.

## -inheritance

The <b>IFaxDevice</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxDevice</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxDevice</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a> object.
