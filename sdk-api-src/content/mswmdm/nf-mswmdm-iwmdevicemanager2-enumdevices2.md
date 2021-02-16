---
UID: NF:mswmdm.IWMDeviceManager2.EnumDevices2
title: IWMDeviceManager2::EnumDevices2 (mswmdm.h)
description: The EnumDevices2 method retrieves an enumeration interface that is used to enumerate portable devices connected to the computer.
helpviewer_keywords: ["EnumDevices2","EnumDevices2 method [windows Media Device Manager]","EnumDevices2 method [windows Media Device Manager]","IWMDeviceManager2 interface","IWMDeviceManager2 interface [windows Media Device Manager]","EnumDevices2 method","IWMDeviceManager2.EnumDevices2","IWMDeviceManager2::EnumDevices2","IWMDeviceManager2EnumDevices2","mswmdm/IWMDeviceManager2::EnumDevices2","wmdm.iwmdevicemanager2_enumdevices2"]
old-location: wmdm\iwmdevicemanager2_enumdevices2.htm
tech.root: WMDM
ms.assetid: b5015263-23f2-466f-a89f-26c14f7a2263
ms.date: 12/05/2018
ms.keywords: EnumDevices2, EnumDevices2 method [windows Media Device Manager], EnumDevices2 method [windows Media Device Manager],IWMDeviceManager2 interface, IWMDeviceManager2 interface [windows Media Device Manager],EnumDevices2 method, IWMDeviceManager2.EnumDevices2, IWMDeviceManager2::EnumDevices2, IWMDeviceManager2EnumDevices2, mswmdm/IWMDeviceManager2::EnumDevices2, wmdm.iwmdevicemanager2_enumdevices2
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
 - IWMDeviceManager2::EnumDevices2
 - mswmdm/IWMDeviceManager2::EnumDevices2
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
 - IWMDeviceManager2.EnumDevices2
---

# IWMDeviceManager2::EnumDevices2


## -description

The <b>EnumDevices2</b> method retrieves an enumeration interface that is used to enumerate portable devices connected to the computer.



Microsoft strongly recommends that applications use the <b>EnumDevices2</b> method instead of <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices">IWMDeviceManager::EnumDevices</a>.

## -parameters

### -param ppEnumDevice [out]

Pointer to a pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice">IWMDMEnumDevice</a> interface. The caller is responsible for calling <b>Release</b> on the retrieved interface.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method returns an enumerator that takes advantage of the Plug and Play (PnP) system for a faster enumeration and lower memory use. For PnP-complaint service providers, it loads in memory only those service providers that have a device currently connected to the computer, and requests only those service providers to create device objects.

This method returns a snapshot of the devices connected when the underlying object was first created. To ensure that the device list is up to date, call <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize">Reinitialize</a> before calling this method.


#### Examples

The following C++ code loops through all the devices and retrieves the display name of each.


```cpp

// Enumerate through the devices using the faster EnumDevices2 Plug-and-Play method.
// IWMDevMgr2 is a global IWMDeviceManager2 pointer.
CComPtr<IWMDMEnumDevice> pEnumDevice;
hr = pIWMDevMgr2->EnumDevices2(&pEnumDevice);
if (hr == S_OK)
{
    // Length of all the strings we'll send in. 
    const UINT MAX_CHARS = 100;
    WCHAR name[MAX_CHARS];

    // Enumerate through devices using a dummy loop.
    while(TRUE)
    {
        // Get a device handle.
        IWMDMDevice* pDevice;
        ULONG ulFetched = 0;
        hr = pEnumDevice->Next(1, &pDevice, &ulFetched);
        CComQIPtr<IWMDMDevice2> pDevice2(pDevice);

        if (hr != S_OK || ulFetched != 1)
        {
            break;
        }
        ZeroMemory(name, MAX_CHARS);
        hr = pDevice2->GetName(name, MAX_CHARS);
    }
}

```

## -see-also

<a href="/windows/desktop/WMDM/enumerating-devices">Enumerating Devices</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice">IWMDMEnumDevice Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2">IWMDeviceManager2 Interface</a>