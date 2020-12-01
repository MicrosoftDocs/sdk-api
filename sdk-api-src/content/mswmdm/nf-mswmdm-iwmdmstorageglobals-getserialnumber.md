---
UID: NF:mswmdm.IWMDMStorageGlobals.GetSerialNumber
title: IWMDMStorageGlobals::GetSerialNumber (mswmdm.h)
description: The GetSerialNumber method retrieves a serial number that uniquely identifies the storage medium.
helpviewer_keywords: ["GetSerialNumber","GetSerialNumber method [windows Media Device Manager]","GetSerialNumber method [windows Media Device Manager]","IWMDMStorageGlobals interface","IWMDMStorageGlobals interface [windows Media Device Manager]","GetSerialNumber method","IWMDMStorageGlobals.GetSerialNumber","IWMDMStorageGlobals::GetSerialNumber","IWMDMStorageGlobalsGetSerialNumber","mswmdm/IWMDMStorageGlobals::GetSerialNumber","wmdm.iwmdmstorageglobals_getserialnumber"]
old-location: wmdm\iwmdmstorageglobals_getserialnumber.htm
tech.root: WMDM
ms.assetid: 13783d0e-82e6-4340-bb06-85b8d3d06b5c
ms.date: 12/05/2018
ms.keywords: GetSerialNumber, GetSerialNumber method [windows Media Device Manager], GetSerialNumber method [windows Media Device Manager],IWMDMStorageGlobals interface, IWMDMStorageGlobals interface [windows Media Device Manager],GetSerialNumber method, IWMDMStorageGlobals.GetSerialNumber, IWMDMStorageGlobals::GetSerialNumber, IWMDMStorageGlobalsGetSerialNumber, mswmdm/IWMDMStorageGlobals::GetSerialNumber, wmdm.iwmdmstorageglobals_getserialnumber
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
 - IWMDMStorageGlobals::GetSerialNumber
 - mswmdm/IWMDMStorageGlobals::GetSerialNumber
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
 - IWMDMStorageGlobals.GetSerialNumber
---

# IWMDMStorageGlobals::GetSerialNumber


## -description

The <b>GetSerialNumber</b> method retrieves a serial number that uniquely identifies the storage medium.

## -parameters

### -param pSerialNum [out]

Pointer to a <a href="/windows/desktop/WMDM/wmdmid">WMDMID</a> structure specifying the serial number information.

### -param abMac [in, out]

Array of bytes specifying the message authentication code for the parameter data of this method. This memory is allocated and freed by the caller.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Not all storage media support serial numbers, but a serial number is required to support Microsoft digital rights management. If the storage medium cannot report a unique serial number, content protected by Microsoft digital rights management cannot be transferred to this storage medium. The return code should be checked to determine whether the storage medium provides this support.


#### Examples

The following C++ code retrieves the serial number of the root storage object, and verifies the MAC.


```cpp

    hr = m_pStorageGlobals->GetSerialNumber(&m_SerialNumber, (BYTE*)abMAC);
    if (SUCCEEDED(hr))
    {
        // Verify the MAC using the CSecureChannelClient member.
        m_pSAC->MACInit(&hMAC);
        m_pSAC->MACUpdate(hMAC, (BYTE*)(&m_SerialNumber), sizeof(m_SerialNumber));
        m_pSAC->MACFinal(hMAC, (BYTE*)abMACVerify);
        if (memcmp(abMACVerify, abMAC, sizeof(abMAC)) != 0)
        {
            hr = E_FAIL;
        }
    }

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals Interface</a>



<a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a>