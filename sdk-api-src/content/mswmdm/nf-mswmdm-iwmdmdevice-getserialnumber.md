---
UID: NF:mswmdm.IWMDMDevice.GetSerialNumber
title: IWMDMDevice::GetSerialNumber (mswmdm.h)
description: The GetSerialNumber method retrieves a serial number that uniquely identifies the device.
helpviewer_keywords: ["GetSerialNumber","GetSerialNumber method [windows Media Device Manager]","GetSerialNumber method [windows Media Device Manager]","IWMDMDevice interface","IWMDMDevice interface [windows Media Device Manager]","GetSerialNumber method","IWMDMDevice.GetSerialNumber","IWMDMDevice::GetSerialNumber","IWMDMDeviceGetSerialNumber","mswmdm/IWMDMDevice::GetSerialNumber","wmdm.iwmdmdevice_getserialnumber"]
old-location: wmdm\iwmdmdevice_getserialnumber.htm
tech.root: WMDM
ms.assetid: e2498ca3-7109-4713-9110-2dbca0436d00
ms.date: 12/05/2018
ms.keywords: GetSerialNumber, GetSerialNumber method [windows Media Device Manager], GetSerialNumber method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetSerialNumber method, IWMDMDevice.GetSerialNumber, IWMDMDevice::GetSerialNumber, IWMDMDeviceGetSerialNumber, mswmdm/IWMDMDevice::GetSerialNumber, wmdm.iwmdmdevice_getserialnumber
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
 - IWMDMDevice::GetSerialNumber
 - mswmdm/IWMDMDevice::GetSerialNumber
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
 - IWMDMDevice.GetSerialNumber
---

# IWMDMDevice::GetSerialNumber


## -description

The <b>GetSerialNumber</b> method retrieves a serial number that uniquely identifies the device.

## -parameters

### -param pSerialNumber [out]

Pointer to a <a href="/windows/desktop/WMDM/wmdmid">WMDMID</a> structure specifying the serial number information. The <b>WMDID</b> structure is allocated and released by the application.

### -param abMac [in, out]

Array of bytes specifying the message authentication code for the parameter data of this method.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Not all devices support serial numbers. To determine whether the device supports serial numbers, the caller must always check the return code when calling this function. If a media device supports serial numbers, the serial number of the media device is guaranteed to be unique for that device.

After calling this method, an application can verify that the serial has not been modified during transport by using the <i>abMAC</i> parameter. For example code on this, see <a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a>.


#### Examples

The following C++ code retrieves the device serial number and verifies the MAC.


```cpp

//
// Get and verify the serial number.
//
WMDMID serialNumber;
BYTE receivedMAC[WMDM_MAC_LENGTH];
hr = pIWMDMDevice->GetSerialNumber(&serialNumber, receivedMAC);

// Check the MAC to guarantee the serial number has not been tampered with.
if (hr == S_OK)
{
    // Initialize a MAC handle, 
    // next add all parameters to the MAC,
    // and finally retrieve the calculated MAC value.
    HMAC hMAC;
    BYTE calculatedMAC[WMDM_MAC_LENGTH];
    hr = m_pSAC->MACInit(&hMAC);
    hr = m_pSAC->MACUpdate(hMAC, (BYTE*)(&serialNumber), sizeof(serialNumber));
    hr = m_pSAC->MACFinal(hMAC, (BYTE*)calculatedMAC);
    if (memcmp(calculatedMAC, receivedMAC, sizeof(calculatedMAC)) == 0)
    {
        // MAC is authentic. Print the serial number.
        CHAR* serialNumberBuffer = new CHAR[serialNumber.SerialNumberLength + 1];
        ZeroMemory(serialNumberBuffer, (serialNumber.SerialNumberLength + 1) * sizeof(CHAR));
        memcpy(serialNumberBuffer, serialNumber.pID, serialNumber.SerialNumberLength * sizeof(CHAR));
        // TODO: Display the serial number.
        delete serialNumberBuffer;
    }
    else
        // TODO: Display a message indicating that the serial number MAC does not match in EnumDevices
}

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice Interface</a>



<a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a>