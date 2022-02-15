---
UID: NN:mswmdm.IMDSPDeviceControl
title: IMDSPDeviceControl (mswmdm.h)
description: The IMDSPDeviceControl interface provides methods for controlling devices.
helpviewer_keywords: ["IMDSPDeviceControl","IMDSPDeviceControl interface [windows Media Device Manager]","IMDSPDeviceControl interface [windows Media Device Manager]","described","IMDSPDeviceControlInterface","mswmdm/IMDSPDeviceControl","wmdm.imdspdevicecontrol"]
old-location: wmdm\imdspdevicecontrol.htm
tech.root: WMDM
ms.assetid: a196edef-f670-4c1f-92bd-172a75f3f420
ms.date: 12/05/2018
ms.keywords: IMDSPDeviceControl, IMDSPDeviceControl interface [windows Media Device Manager], IMDSPDeviceControl interface [windows Media Device Manager],described, IMDSPDeviceControlInterface, mswmdm/IMDSPDeviceControl, wmdm.imdspdevicecontrol
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
 - IMDSPDeviceControl
 - mswmdm/IMDSPDeviceControl
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
 - IMDSPDeviceControl
---

# IMDSPDeviceControl interface


## -description

The <b>IMDSPDeviceControl</b> interface provides methods for controlling devices. After this interface is acquired from a specific instance of the <b>IMDSPDevice</b> interface, the control methods are used for remote control of streaming audio play, record, pause, stop, and seek operations on that device. Implementing this interface is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

The <b>IMDSPDeviceControl</b> interface methods support several modes of audio control, depending on the context in which they are used. That context is defined by the <b>Seek</b> method. The <b>GetCapabilities</b> method is used to determine what kinds of operations can be performed by the device.

## -inheritance

The <b>IMDSPDeviceControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPDeviceControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
