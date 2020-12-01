---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulkCallback.OnStart
title: IPortableDevicePropertiesBulkCallback::OnStart (portabledeviceapi.h)
description: The OnStart method is called by the SDK when a bulk operation started by IPortableDevicePropertiesBulk::Start is about to begin.
helpviewer_keywords: ["IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK]","OnStart method","IPortableDevicePropertiesBulkCallback.OnStart","IPortableDevicePropertiesBulkCallback::OnStart","IPortableDevicePropertiesBulkCallbackOnStart","OnStart","OnStart method [Windows Portable Devices SDK]","OnStart method [Windows Portable Devices SDK]","IPortableDevicePropertiesBulkCallback interface","portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnStart","wpdsdk.iportabledevicepropertiesbulkcallback_onstart"]
old-location: wpdsdk\iportabledevicepropertiesbulkcallback_onstart.htm
tech.root: wpdsdk
ms.assetid: bde04e04-d36e-4471-b598-ee38dba9f614
ms.date: 12/05/2018
ms.keywords: IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK],OnStart method, IPortableDevicePropertiesBulkCallback.OnStart, IPortableDevicePropertiesBulkCallback::OnStart, IPortableDevicePropertiesBulkCallbackOnStart, OnStart, OnStart method [Windows Portable Devices SDK], OnStart method [Windows Portable Devices SDK],IPortableDevicePropertiesBulkCallback interface, portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnStart, wpdsdk.iportabledevicepropertiesbulkcallback_onstart
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
 - IPortableDevicePropertiesBulkCallback::OnStart
 - portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnStart
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
 - IPortableDevicePropertiesBulkCallback.OnStart
---

# IPortableDevicePropertiesBulkCallback::OnStart


## -description

The <b>OnStart</b> method is called by the SDK when a bulk operation started by <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start">IPortableDevicePropertiesBulk::Start</a> is about to begin.

## -parameters

### -param pContext [in]

Pointer to a GUID that identifies which operation has started. This value is produced by a <b>Queue</b>... method of the <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulk">IPortableDevicePropertiesBulk</a> interface.

## -returns

The application should return either S_OK or an error code to abandon the operation. The application should handle all error codes in the same manner.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback">IPortableDevicePropertiesBulkCallback Interface</a>