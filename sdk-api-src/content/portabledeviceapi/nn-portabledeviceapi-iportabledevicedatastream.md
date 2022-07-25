---
UID: NN:portabledeviceapi.IPortableDeviceDataStream
title: IPortableDeviceDataStream (portabledeviceapi.h)
description: The IPortableDeviceDataStream interface exposes additional methods on an IStream that is used for data transfers.
helpviewer_keywords: ["IPortableDeviceDataStream","IPortableDeviceDataStream interface [Windows Portable Devices SDK]","IPortableDeviceDataStream interface [Windows Portable Devices SDK]","described","IPortableDeviceDataStreamInterface","portabledeviceapi/IPortableDeviceDataStream","wpdsdk.iportabledevicedatastream"]
old-location: wpdsdk\iportabledevicedatastream.htm
tech.root: wpdsdk
ms.assetid: d7bd955a-886f-4081-bfc3-cd2d7e2cfb24
ms.date: 12/05/2018
ms.keywords: IPortableDeviceDataStream, IPortableDeviceDataStream interface [Windows Portable Devices SDK], IPortableDeviceDataStream interface [Windows Portable Devices SDK],described, IPortableDeviceDataStreamInterface, portabledeviceapi/IPortableDeviceDataStream, wpdsdk.iportabledevicedatastream
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
 - IPortableDeviceDataStream
 - portabledeviceapi/IPortableDeviceDataStream
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
 - IPortableDeviceDataStream
---

# IPortableDeviceDataStream interface


## -description

The <b>IPortableDeviceDataStream</b> interface exposes additional methods on an <b>IStream</b> that is used for data transfers. It is obtained by calling <b>QueryInterface</b> on the <b>IStream</b> that is retrieved by <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceresources-getstream">IPortableDeviceResources::GetStream</a> or <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata">IPortableDeviceContent::CreateObjectWithPropertiesAndData</a>.

## -inheritance

The <b>IPortableDeviceDataStream</b> interface inherits from <b>IStream</b>. <b>IPortableDeviceDataStream</b> also has these types of members:

