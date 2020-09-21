---
UID: NF:mswmdm.IWMDMDevice.GetName
title: IWMDMDevice::GetName (mswmdm.h)
description: The GetName method retrieves the human-readable name of the media device.
helpviewer_keywords: ["GetName","GetName method [windows Media Device Manager]","GetName method [windows Media Device Manager]","IWMDMDevice interface","IWMDMDevice interface [windows Media Device Manager]","GetName method","IWMDMDevice.GetName","IWMDMDevice::GetName","IWMDMDeviceGetName","mswmdm/IWMDMDevice::GetName","wmdm.iwmdmdevice_getname"]
old-location: wmdm\iwmdmdevice_getname.htm
tech.root: WMDM
ms.assetid: 4bc5d550-6631-40ea-b020-2f5bb55899d6
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [windows Media Device Manager], GetName method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetName method, IWMDMDevice.GetName, IWMDMDevice::GetName, IWMDMDeviceGetName, mswmdm/IWMDMDevice::GetName, wmdm.iwmdmdevice_getname
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
 - IWMDMDevice::GetName
 - mswmdm/IWMDMDevice::GetName
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
 - IWMDMDevice.GetName
---

# IWMDMDevice::GetName


## -description

The <b>GetName</b> method retrieves the human-readable name of the media device.

## -parameters

### -param pwszName [out]

Pointer to a (Unicode) wide-character, null-terminated string specifying the device name. The buffer is allocated and released by the caller.

### -param nMaxChars [in]

Integer specifying the maximum number of characters that can be placed in <i>pwszName</i>, including the termination character.

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



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype">IWMDMDevice::GetType</a>