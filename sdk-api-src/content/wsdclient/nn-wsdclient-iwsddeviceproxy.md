---
UID: NN:wsdclient.IWSDDeviceProxy
title: IWSDDeviceProxy (wsdclient.h)
description: Represents a remote Devices Profile for Web Services (DPWS) device for client applications and middleware.
helpviewer_keywords: ["IWSDDeviceProxy","IWSDDeviceProxy interface","IWSDDeviceProxy interface","described","ncd.iwsddeviceproxy","wsdclient/IWSDDeviceProxy"]
old-location: ncd\iwsddeviceproxy.htm
tech.root: ncd
ms.assetid: a1a54ba0-241a-4c3d-8113-89c0f8171c40
ms.date: 12/05/2018
ms.keywords: IWSDDeviceProxy, IWSDDeviceProxy interface, IWSDDeviceProxy interface,described, ncd.iwsddeviceproxy, wsdclient/IWSDDeviceProxy
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDDeviceProxy
 - wsdclient/IWSDDeviceProxy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceProxy
---

# IWSDDeviceProxy interface


## -description

Represents a remote Devices Profile for Web Services (DPWS) device for client applications and middleware.

To get this interface, you can call <a href="/windows/desktop/api/wsdclient/nf-wsdclient-wsdcreatedeviceproxy">WSDCreateDeviceProxy</a>.

## -inheritance

The <b>IWSDDeviceProxy</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDDeviceProxy</b> also has these types of members:

## -remarks

This interface is a client-side representation of a remote device. The proxy provides basic access to device metadata (<a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_this_device_metadata">WSD_THIS_DEVICE_METADATA</a> and <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_this_model_metadata">WSD_THIS_MODEL_METADATA</a>), in addition to providing methods for creating service proxy objects. The service proxy objects correspond to service hosted on the device. For example, a television is a device and the tuner portion of the television is a service hosted on the device that has an accessible, atomic set of functions.

The <b>IWSDDeviceProxy</b> object exposes WSD-specific device semantics.

To use <b>IWSDDeviceProxy</b> in your client or middleware application: 



<ol>
<li>Call <a href="/windows/desktop/api/wsdclient/nf-wsdclient-wsdcreatedeviceproxy">WSDCreateDeviceProxy</a>.</li>
<li>Call any of the four metadata methods of the device proxy object.</li>
<li>Get an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a> object, either by calling <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getserviceproxybyid">GetServiceProxyById</a> or <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-getserviceproxybytype">GetServiceProxyByType</a>.</li>
</ol>

## -see-also

<a href="/windows/desktop/WsdApi/overview-of-the-wsdapi-interfaces">Overview of the WSDAPI Interfaces</a>
