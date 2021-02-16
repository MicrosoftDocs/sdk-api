---
UID: NF:mswmdm.IWMDeviceManager.EnumDevices
title: IWMDeviceManager::EnumDevices (mswmdm.h)
description: The EnumDevices method retrieves a pointer to the IWMDMEnumDevice interface that can be used to enumerate portable devices connected to the computer.
helpviewer_keywords: ["EnumDevices","EnumDevices method [windows Media Device Manager]","EnumDevices method [windows Media Device Manager]","IWMDeviceManager interface","IWMDeviceManager interface [windows Media Device Manager]","EnumDevices method","IWMDeviceManager.EnumDevices","IWMDeviceManager::EnumDevices","IWMDeviceManagerEnumDevices","mswmdm/IWMDeviceManager::EnumDevices","wmdm.iwmdevicemanager_enumdevices"]
old-location: wmdm\iwmdevicemanager_enumdevices.htm
tech.root: WMDM
ms.assetid: 1daa6d36-9858-4504-a9a2-c0341031829b
ms.date: 12/05/2018
ms.keywords: EnumDevices, EnumDevices method [windows Media Device Manager], EnumDevices method [windows Media Device Manager],IWMDeviceManager interface, IWMDeviceManager interface [windows Media Device Manager],EnumDevices method, IWMDeviceManager.EnumDevices, IWMDeviceManager::EnumDevices, IWMDeviceManagerEnumDevices, mswmdm/IWMDeviceManager::EnumDevices, wmdm.iwmdevicemanager_enumdevices
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
 - IWMDeviceManager::EnumDevices
 - mswmdm/IWMDeviceManager::EnumDevices
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
 - IWMDeviceManager.EnumDevices
---

# IWMDeviceManager::EnumDevices


## -description

The <b>EnumDevices</b> method retrieves a pointer to the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice">IWMDMEnumDevice</a> interface that can be used to enumerate portable devices connected to the computer.

## -parameters

### -param ppEnumDevice [out]

Pointer to a pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice">IWMDMEnumDevice</a> interface used to enumerate devices. The caller must release this interface when done with it.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method returns devices based on earlier versions of Windows Media Device Manager. To get all devices, including newer devices (such as MTP devices), call <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2">IWMDMDeviceManager2::EnumDevices2</a>.

## -see-also

<a href="/windows/desktop/WMDM/enumerating-devices">Enumerating Devices</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice">IWMDMEnumDevice Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager">IWMDeviceManager Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2">IWMDeviceManager2::EnumDevices2</a>