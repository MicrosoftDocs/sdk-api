---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulkCallback.OnEnd
title: IPortableDevicePropertiesBulkCallback::OnEnd (portabledeviceapi.h)
description: The OnEnd method is called by the SDK when a bulk operation that is started by IPortableDevicePropertiesBulk::Start is completed.
helpviewer_keywords: ["IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK]","OnEnd method","IPortableDevicePropertiesBulkCallback.OnEnd","IPortableDevicePropertiesBulkCallback::OnEnd","IPortableDevicePropertiesBulkCallbackOnEnd","OnEnd","OnEnd method [Windows Portable Devices SDK]","OnEnd method [Windows Portable Devices SDK]","IPortableDevicePropertiesBulkCallback interface","portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnEnd","wpdsdk.iportabledevicepropertiesbulkcallback_onend"]
old-location: wpdsdk\iportabledevicepropertiesbulkcallback_onend.htm
tech.root: wpdsdk
ms.assetid: a3e56415-fe75-4d54-8448-6ca7793147fd
ms.date: 12/05/2018
ms.keywords: IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK],OnEnd method, IPortableDevicePropertiesBulkCallback.OnEnd, IPortableDevicePropertiesBulkCallback::OnEnd, IPortableDevicePropertiesBulkCallbackOnEnd, OnEnd, OnEnd method [Windows Portable Devices SDK], OnEnd method [Windows Portable Devices SDK],IPortableDevicePropertiesBulkCallback interface, portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnEnd, wpdsdk.iportabledevicepropertiesbulkcallback_onend
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
 - IPortableDevicePropertiesBulkCallback::OnEnd
 - portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnEnd
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
 - IPortableDevicePropertiesBulkCallback.OnEnd
---

# IPortableDevicePropertiesBulkCallback::OnEnd


## -description

The <b>OnEnd</b> method is called by the SDK when a bulk operation that is started by <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start">IPortableDevicePropertiesBulk::Start</a> is completed.

## -parameters

### -param pContext [in]

Pointer to a GUID that identifies which operation has finished. This value is produced by a <b>Queue</b>... method of the <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulk">IPortableDevicePropertiesBulk</a> interface.

### -param hrStatus [out]

Contains any errors returned by the driver after the bulk operation has completed.

## -returns

The method's return value is ignored.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback">IPortableDevicePropertiesBulkCallback Interface</a>