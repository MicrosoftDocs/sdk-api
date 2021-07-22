---
UID: NN:mswmdm.IWMDMDeviceControl
title: IWMDMDeviceControl (mswmdm.h)
description: The IWMDMDeviceControl interface provides methods for controlling playback on a device.
helpviewer_keywords: ["IWMDMDeviceControl","IWMDMDeviceControl interface [windows Media Device Manager]","IWMDMDeviceControl interface [windows Media Device Manager]","described","IWMDMDeviceControlInterface","mswmdm/IWMDMDeviceControl","wmdm.iwmdmdevicecontrol"]
old-location: wmdm\iwmdmdevicecontrol.htm
tech.root: WMDM
ms.assetid: e7b58957-4795-461f-ae3d-fb80e6711c9f
ms.date: 12/05/2018
ms.keywords: IWMDMDeviceControl, IWMDMDeviceControl interface [windows Media Device Manager], IWMDMDeviceControl interface [windows Media Device Manager],described, IWMDMDeviceControlInterface, mswmdm/IWMDMDeviceControl, wmdm.iwmdmdevicecontrol
req.header: mswmdm.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMDeviceControl
 - mswmdm/IWMDMDeviceControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMDeviceControl
---

# IWMDMDeviceControl interface


## -description

The <b>IWMDMDeviceControl</b> interface provides methods for controlling playback on a device. Query an <b>IWMDMDevice</b> interface to get this interface. Playback parameters are controlled by the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo">IWMDMObjectInfo</a> interface.

The <b>IWMDMDeviceControl</b> interface methods support several modes of audio control, depending on the context in which they are used. That context is defined by the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-seek">IWMDMDeviceControl::Seek</a> method. The <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicecontrol-getcapabilities">IWMDMDeviceControl::GetCapabilities</a> method is used to determine what kinds of operations can be performed by the device.

## -inheritance

The <b>IWMDMDeviceControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMDeviceControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
