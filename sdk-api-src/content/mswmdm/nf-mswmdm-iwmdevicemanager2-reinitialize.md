---
UID: NF:mswmdm.IWMDeviceManager2.Reinitialize
title: IWMDeviceManager2::Reinitialize (mswmdm.h)
description: The Reinitialize method forces Windows Media Device Manager to rediscover all the Windows Media Device Manager devices.
helpviewer_keywords: ["IWMDeviceManager2 interface [windows Media Device Manager]","Reinitialize method","IWMDeviceManager2.Reinitialize","IWMDeviceManager2::Reinitialize","IWMDeviceManager2Reinitialize","Reinitialize","Reinitialize method [windows Media Device Manager]","Reinitialize method [windows Media Device Manager]","IWMDeviceManager2 interface","mswmdm/IWMDeviceManager2::Reinitialize","wmdm.iwmdevicemanager2_reinitialize"]
old-location: wmdm\iwmdevicemanager2_reinitialize.htm
tech.root: WMDM
ms.assetid: 9eabf5ff-96e1-426f-ae31-197a2165a743
ms.date: 12/05/2018
ms.keywords: IWMDeviceManager2 interface [windows Media Device Manager],Reinitialize method, IWMDeviceManager2.Reinitialize, IWMDeviceManager2::Reinitialize, IWMDeviceManager2Reinitialize, Reinitialize, Reinitialize method [windows Media Device Manager], Reinitialize method [windows Media Device Manager],IWMDeviceManager2 interface, mswmdm/IWMDeviceManager2::Reinitialize, wmdm.iwmdevicemanager2_reinitialize
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDeviceManager2::Reinitialize
 - mswmdm/IWMDeviceManager2::Reinitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDeviceManager2.Reinitialize
---

# IWMDeviceManager2::Reinitialize


## -description

The <b>Reinitialize</b> method forces Windows Media Device Manager to rediscover all the Windows Media Device Manager devices.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

Windows Media Device Manager monitors Plug and Play (PnP) notifications to keep track of connected devices which are controlled by a PnP-compliant service provider. If a non-compliant device is plugged in or some other changes are made to a device for which the device does not generate PnP notifications (for example, insertion or removal of a storage card), the application should call this method before calling <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2">IWMDeviceManager2::EnumDevices2</a>. The application would typically do this on a refresh request from the user.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2">IWMDeviceManager2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2">IWMDeviceManager2::EnumDevices2</a>
