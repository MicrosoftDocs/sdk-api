---
UID: NN:faxcomex.IFaxDeviceIds
title: IFaxDeviceIds (faxcomex.h)
description: The IFaxDeviceIds interface defines a configuration collection used by a fax client application to enumerate the ordered fax device IDs associated with a FaxOutboundRoutingGroup object.
helpviewer_keywords: ["IFaxDeviceIds","IFaxDeviceIds interface [Fax Service]","IFaxDeviceIds interface [Fax Service]","described","_mfax_faxdeviceids_cpp","fax._mfax_faxdeviceids_cpp","faxcomex/IFaxDeviceIds"]
old-location: fax\_mfax_faxdeviceids_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_606r_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxDeviceIds, IFaxDeviceIds interface [Fax Service], IFaxDeviceIds interface [Fax Service],described, _mfax_faxdeviceids_cpp, fax._mfax_faxdeviceids_cpp, faxcomex/IFaxDeviceIds
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
 - IFaxDeviceIds
 - faxcomex/IFaxDeviceIds
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
 - IFaxDeviceIds
---

# IFaxDeviceIds interface


## -description

The <b>IFaxDeviceIds</b> interface defines a configuration collection used by a fax client application to enumerate the ordered fax device IDs associated with a <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroup">FaxOutboundRoutingGroup</a> object. The collection includes methods to add, remove, and change the order of devices. The order of the devices in the collection determines the relative order in which available fax devices send outgoing transmissions.

## -inheritance

The <b>IFaxDeviceIds</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxDeviceIds</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxDeviceIds</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> object.
