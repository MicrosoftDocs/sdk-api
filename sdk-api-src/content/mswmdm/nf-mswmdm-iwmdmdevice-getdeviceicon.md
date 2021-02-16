---
UID: NF:mswmdm.IWMDMDevice.GetDeviceIcon
title: IWMDMDevice::GetDeviceIcon (mswmdm.h)
description: The GetDeviceIcon method retrieves a handle to the icon that the device manufacturer wants to display when the device is connected.
helpviewer_keywords: ["GetDeviceIcon","GetDeviceIcon method [windows Media Device Manager]","GetDeviceIcon method [windows Media Device Manager]","IWMDMDevice interface","IWMDMDevice interface [windows Media Device Manager]","GetDeviceIcon method","IWMDMDevice.GetDeviceIcon","IWMDMDevice::GetDeviceIcon","IWMDMDeviceGetDeviceIcon","mswmdm/IWMDMDevice::GetDeviceIcon","wmdm.iwmdmdevice_getdeviceicon"]
old-location: wmdm\iwmdmdevice_getdeviceicon.htm
tech.root: WMDM
ms.assetid: 55da3443-ad5b-469d-a493-0e2e8ea21f0c
ms.date: 12/05/2018
ms.keywords: GetDeviceIcon, GetDeviceIcon method [windows Media Device Manager], GetDeviceIcon method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetDeviceIcon method, IWMDMDevice.GetDeviceIcon, IWMDMDevice::GetDeviceIcon, IWMDMDeviceGetDeviceIcon, mswmdm/IWMDMDevice::GetDeviceIcon, wmdm.iwmdmdevice_getdeviceicon
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
 - IWMDMDevice::GetDeviceIcon
 - mswmdm/IWMDMDevice::GetDeviceIcon
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
 - IWMDMDevice.GetDeviceIcon
---

# IWMDMDevice::GetDeviceIcon


## -description

The <b>GetDeviceIcon</b> method retrieves a handle to the icon that the device manufacturer wants to display when the device is connected.

## -parameters

### -param hIcon [out]

Handle to an icon object.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

When the application is finished with the icon, it must call the Win32 <b>DestroyIcon</b> function to free the memory.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice Interface</a>