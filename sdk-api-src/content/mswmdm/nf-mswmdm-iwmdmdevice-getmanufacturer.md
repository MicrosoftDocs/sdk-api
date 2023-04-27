---
UID: NF:mswmdm.IWMDMDevice.GetManufacturer
title: IWMDMDevice::GetManufacturer (mswmdm.h)
description: The GetManufacturer method retrieves the name of the manufacturer of the device. (IWMDMDevice.GetManufacturer)
helpviewer_keywords: ["GetManufacturer","GetManufacturer method [windows Media Device Manager]","GetManufacturer method [windows Media Device Manager]","IWMDMDevice interface","IWMDMDevice interface [windows Media Device Manager]","GetManufacturer method","IWMDMDevice.GetManufacturer","IWMDMDevice::GetManufacturer","IWMDMDeviceGetManufacturer","mswmdm/IWMDMDevice::GetManufacturer","wmdm.iwmdmdevice_getmanufacturer"]
old-location: wmdm\iwmdmdevice_getmanufacturer.htm
tech.root: WMDM
ms.assetid: 42e862e4-bfbc-4fca-b5df-001416173d6e
ms.date: 12/05/2018
ms.keywords: GetManufacturer, GetManufacturer method [windows Media Device Manager], GetManufacturer method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetManufacturer method, IWMDMDevice.GetManufacturer, IWMDMDevice::GetManufacturer, IWMDMDeviceGetManufacturer, mswmdm/IWMDMDevice::GetManufacturer, wmdm.iwmdmdevice_getmanufacturer
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
 - IWMDMDevice::GetManufacturer
 - mswmdm/IWMDMDevice::GetManufacturer
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
 - IWMDMDevice.GetManufacturer
---

# IWMDMDevice::GetManufacturer


## -description

The <b>GetManufacturer</b> method retrieves the name of the manufacturer of the device.

## -parameters

### -param pwszName [out]

Pointer to a wide-character, null-terminated string specifying the manufacturer's name. The buffer must be allocated and released by the caller.

### -param nMaxChars [in]

Integer specifying the maximum number of characters that can be copied to <i>pwszName</i>, including the termination character.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/WMDM/exploring-a-device">Exploring a Device</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice Interface</a>
