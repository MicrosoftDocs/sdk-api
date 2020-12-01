---
UID: NF:mswmdm.IWMDMDevice.GetVersion
title: IWMDMDevice::GetVersion (mswmdm.h)
description: The GetVersion method retrieves the manufacturer-defined version number of the device.
helpviewer_keywords: ["GetVersion","GetVersion method [windows Media Device Manager]","GetVersion method [windows Media Device Manager]","IWMDMDevice interface","IWMDMDevice interface [windows Media Device Manager]","GetVersion method","IWMDMDevice.GetVersion","IWMDMDevice::GetVersion","IWMDMDeviceGetVersion","mswmdm/IWMDMDevice::GetVersion","wmdm.iwmdmdevice_getversion"]
old-location: wmdm\iwmdmdevice_getversion.htm
tech.root: WMDM
ms.assetid: ae0253f2-30cd-46d0-b9e9-f2cb878c1ff3
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion method [windows Media Device Manager], GetVersion method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetVersion method, IWMDMDevice.GetVersion, IWMDMDevice::GetVersion, IWMDMDeviceGetVersion, mswmdm/IWMDMDevice::GetVersion, wmdm.iwmdmdevice_getversion
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
 - IWMDMDevice::GetVersion
 - mswmdm/IWMDMDevice::GetVersion
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
 - IWMDMDevice.GetVersion
---

# IWMDMDevice::GetVersion


## -description

The <b>GetVersion</b> method retrieves the manufacturer-defined version number of the device.

## -parameters

### -param pdwVersion [out]

Pointer to a <b>DWORD</b> specifying the version number.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The format of the version number is determined by the manufacturer.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice Interface</a>