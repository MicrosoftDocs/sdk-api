---
UID: NN:mswmdm.IWMDeviceManager
title: IWMDeviceManager (mswmdm.h)
description: The IWMDeviceManager interface is the top level Windows Media Device Manager interface for applications.
helpviewer_keywords: ["IWMDeviceManager","IWMDeviceManager interface [windows Media Device Manager]","IWMDeviceManager interface [windows Media Device Manager]","described","IWMDeviceManagerInterface","mswmdm/IWMDeviceManager","wmdm.iwmdevicemanager"]
old-location: wmdm\iwmdevicemanager.htm
tech.root: WMDM
ms.assetid: cac68821-42fc-4833-bf2e-eec1768869e6
ms.date: 12/05/2018
ms.keywords: IWMDeviceManager, IWMDeviceManager interface [windows Media Device Manager], IWMDeviceManager interface [windows Media Device Manager],described, IWMDeviceManagerInterface, mswmdm/IWMDeviceManager, wmdm.iwmdevicemanager
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
 - IWMDeviceManager
 - mswmdm/IWMDeviceManager
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
 - IWMDeviceManager
---

# IWMDeviceManager interface


## -description

The <b>IWMDeviceManager</b> interface is the top level Windows Media Device Manager interface for applications. This is the first interface accessed by an application, and is used to acquire the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice">IWMDMEnumDevice</a> interface used to enumerate the connected devices. This interface is obtained by calling <b>QueryInterface</b> on the authenticated <a href="/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate">IComponentAuthenticate</a> interface. If the device supports it, use <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2">IWMDeviceManager2</a> interface, which offers superior device enumeration capabilities.

## -inheritance

The <b>IWMDeviceManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDeviceManager</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2">IWMDeviceManager2 Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
