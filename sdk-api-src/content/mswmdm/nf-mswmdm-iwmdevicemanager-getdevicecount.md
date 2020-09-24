---
UID: NF:mswmdm.IWMDeviceManager.GetDeviceCount
title: IWMDeviceManager::GetDeviceCount (mswmdm.h)
description: The GetDeviceCount method retrieves the number of portable devices that are currently connected to the computer.
helpviewer_keywords: ["GetDeviceCount","GetDeviceCount method [windows Media Device Manager]","GetDeviceCount method [windows Media Device Manager]","IWMDeviceManager interface","IWMDeviceManager interface [windows Media Device Manager]","GetDeviceCount method","IWMDeviceManager.GetDeviceCount","IWMDeviceManager::GetDeviceCount","IWMDeviceManagerGetDeviceCount","mswmdm/IWMDeviceManager::GetDeviceCount","wmdm.iwmdevicemanager_getdevicecount"]
old-location: wmdm\iwmdevicemanager_getdevicecount.htm
tech.root: WMDM
ms.assetid: efa8ccf6-c796-4ed7-8fe0-2e6570292aaa
ms.date: 12/05/2018
ms.keywords: GetDeviceCount, GetDeviceCount method [windows Media Device Manager], GetDeviceCount method [windows Media Device Manager],IWMDeviceManager interface, IWMDeviceManager interface [windows Media Device Manager],GetDeviceCount method, IWMDeviceManager.GetDeviceCount, IWMDeviceManager::GetDeviceCount, IWMDeviceManagerGetDeviceCount, mswmdm/IWMDeviceManager::GetDeviceCount, wmdm.iwmdevicemanager_getdevicecount
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
 - IWMDeviceManager::GetDeviceCount
 - mswmdm/IWMDeviceManager::GetDeviceCount
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
 - IWMDeviceManager.GetDeviceCount
---

# IWMDeviceManager::GetDeviceCount


## -description

The <b>GetDeviceCount</b> method retrieves the number of portable devices that are currently connected to the computer.

## -parameters

### -param pdwCount [out]

Pointer to a <b>DWORD</b> specifying the count of known devices.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/WMDM/enumerating-devices">Enumerating Devices</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager">IWMDeviceManager Interface</a>