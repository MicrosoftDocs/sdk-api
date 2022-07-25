---
UID: NN:portabledeviceapi.IPortableDeviceManager
title: IPortableDeviceManager (portabledeviceapi.h)
description: Enumerates devices that are connected to the computer and provides a simple way to request installation information, including manufacturer, friendly name, and description.
helpviewer_keywords: ["IPortableDeviceManager","IPortableDeviceManager interface [Windows Portable Devices SDK]","IPortableDeviceManager interface [Windows Portable Devices SDK]","described","IPortableDeviceManagerInterface","portabledeviceapi/IPortableDeviceManager","wpdsdk.iportabledevicemanager"]
old-location: wpdsdk\iportabledevicemanager.htm
tech.root: wpdsdk
ms.assetid: 11cd5b2b-e8f8-4ba1-8527-f7a403f399d5
ms.date: 12/05/2018
ms.keywords: IPortableDeviceManager, IPortableDeviceManager interface [Windows Portable Devices SDK], IPortableDeviceManager interface [Windows Portable Devices SDK],described, IPortableDeviceManagerInterface, portabledeviceapi/IPortableDeviceManager, wpdsdk.iportabledevicemanager
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceManager
 - portabledeviceapi/IPortableDeviceManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceManager
---

# IPortableDeviceManager interface


## -description

Enumerates devices that are connected to the computer and provides a simple way to request installation information, including manufacturer, friendly name, and description. This is typically the first Windows Portable Devices interface created by an application. To create an instance of this interface, call <b>CoCreateInstance</b> and specify <b>CLSID_PortableDeviceManager</b>.

The properties that are requested using this interface can also be requested by using the <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties">IPortableDeviceProperties</a> interface. However, that interface requires several steps to acquire; using this interface is a much simpler way to request device information.

## -inheritance

The <b>IPortableDeviceManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceManager</b> also has these types of members:

## -see-also

<a href="/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>
