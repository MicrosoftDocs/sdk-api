---
UID: NF:mswmdm.IWMDMEnumDevice.Next
title: IWMDMEnumDevice::Next (mswmdm.h)
description: The Next method returns a pointer to the next device, represented by an IWMDMDevice interface.
helpviewer_keywords: ["IWMDMEnumDevice interface [windows Media Device Manager]","Next method","IWMDMEnumDevice.Next","IWMDMEnumDevice::Next","IWMDMEnumDeviceNext","Next","Next method [windows Media Device Manager]","Next method [windows Media Device Manager]","IWMDMEnumDevice interface","mswmdm/IWMDMEnumDevice::Next","wmdm.iwmdmenumdevice_next"]
old-location: wmdm\iwmdmenumdevice_next.htm
tech.root: WMDM
ms.assetid: 75a5961f-2c61-4e10-a570-7ebfabb97367
ms.date: 12/05/2018
ms.keywords: IWMDMEnumDevice interface [windows Media Device Manager],Next method, IWMDMEnumDevice.Next, IWMDMEnumDevice::Next, IWMDMEnumDeviceNext, Next, Next method [windows Media Device Manager], Next method [windows Media Device Manager],IWMDMEnumDevice interface, mswmdm/IWMDMEnumDevice::Next, wmdm.iwmdmenumdevice_next
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
 - IWMDMEnumDevice::Next
 - mswmdm/IWMDMEnumDevice::Next
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
 - IWMDMEnumDevice.Next
---

# IWMDMEnumDevice::Next


## -description

The <b>Next</b> method returns a pointer to the next device, represented by an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice</a> interface.

## -parameters

### -param celt [in]

Number of devices requested.

### -param ppDevice [out]

Pointer to caller-allocated array of <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice</a> interface pointers. The size of this array must be <b>IWMDMDevice</b> *[celt]. The caller must release these interfaces when done with them. To avoid allocating a whole array, simply pass in the address of a pointer to an <b>IWMDMDevice</b> interface, as shown in Remarks.

### -param pceltFetched [out]

Pointer to a variable that receives the number of devices (interfaces) returned.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The returned device interface(s) are based on a cached list of devices. If a Plug and Play device is attached or removed, the current enumerator will not reflect that, and therefore, <b>Next</b> will return devices based on the cached list. Applications should obtain a new enumerator object by calling <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices">IWMDeviceManager::EnumDevices</a> to get a refreshed list of devices.

If you only want to retrieve a single interface at a time, you do not need to allocate an array for this method, as shown in the following code:


```cpp

// Get a device enumerator to examine each device.
CComPtr<IWMDeviceManager2> pIWMDevMgr2;
hr = m_IWMDeviceMgr->QueryInterface (__uuidof(IWMDeviceManager2), (void**) &pIWMDevMgr2);
if (hr == S_OK)
{
    // TODO: Display a message that the application retrieved IWMDeviceManager2.
}
else
{
    // TODO: Display a message that the application was not able to 
    // retrieve IWMDeviceManager2 in EnumDevices.
    return hr;
}

// Enumerate through the devices using the faster EnumDevices2 plug-and-play method.
CComPtr<IWMDMEnumDevice> pEnumDevice;
hr = pIWMDevMgr2->EnumDevices2(&pEnumDevice);
if (hr != S_OK)
{
    //.TODO: Display a message that an error occurred in calling EnumDevices2.
    return hr;
}

// Enumerate through devices.
IWMDMDevice *pIWMDMDevice;
ULONG ulFetched = 0;
while(pEnumDevice->Next(1, &pIWMDMDevice, &ulFetched) == S_OK)
{
    if (ulFetched != 1)
    {
        return E_FAIL;
    }
    // Do some stuff here....
}

```

## -see-also

<a href="/windows/desktop/WMDM/enumerating-devices">Enumerating Devices</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice">IWMDMEnumDevice Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices">IWMDeviceManager::EnumDevices</a>