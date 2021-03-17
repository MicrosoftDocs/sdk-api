---
UID: NF:mswmdm.IWMDMStorage.GetRights
title: IWMDMStorage::GetRights (mswmdm.h)
description: The GetRights method retrieves rights information for a licensed storage.
helpviewer_keywords: ["GetRights","GetRights method [windows Media Device Manager]","GetRights method [windows Media Device Manager]","IWMDMStorage interface","IWMDMStorage interface [windows Media Device Manager]","GetRights method","IWMDMStorage.GetRights","IWMDMStorage::GetRights","IWMDMStorageGetRights","mswmdm/IWMDMStorage::GetRights","wmdm.iwmdmstorage_getrights"]
old-location: wmdm\iwmdmstorage_getrights.htm
tech.root: WMDM
ms.assetid: 5b654d32-b72a-44cf-a8d9-63fc0ae76171
ms.date: 12/05/2018
ms.keywords: GetRights, GetRights method [windows Media Device Manager], GetRights method [windows Media Device Manager],IWMDMStorage interface, IWMDMStorage interface [windows Media Device Manager],GetRights method, IWMDMStorage.GetRights, IWMDMStorage::GetRights, IWMDMStorageGetRights, mswmdm/IWMDMStorage::GetRights, wmdm.iwmdmstorage_getrights
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
 - IWMDMStorage::GetRights
 - mswmdm/IWMDMStorage::GetRights
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
 - IWMDMStorage.GetRights
---

# IWMDMStorage::GetRights


## -description

The <b>GetRights</b> method retrieves rights information for a licensed storage.

## -parameters

### -param ppRights [out]

Pointer to an array of <a href="/windows/desktop/WMDM/wmdmrights">WMDMRIGHTS</a> structures that contain the storage rights. This parameter is included in the message authentication code. Windows Media Device Manager allocates this memory, and the application must release it with <b>CoTaskMemFree</b>.

### -param pnRightsCount [out]

Pointer to the number of <b>WMDMRIGHTS</b> structures in the <i>ppRights</i> array. This parameter is included in the message authentication code.

### -param abMac [in, out]

Array of bytes containing the message authentication code (MAC) for the parameter data of this method.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Object rights describe the usage permissions for digital media content. For example, the <b>WMDMRIGHTS</b> structure can contain information concerning how many times a file can be played and who can play it. This method will fail if this is not a licensed file.

The <i>ppRights</i> array is allocated by this method, and must be freed by the application using <b>CoTaskMemFree</b>, a standard Win32 function.

To receive progress events for this call, use <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getrightswithprogress">IWMDMStorage4::GetRightsWithProgress</a>.

After calling this method, an application can calculate the message authentication code (MAC) values of parameters and compare them with output MAC values to ensure that the parameters have not been tampered with. The following example code shows one way to do this.


#### Examples


```cpp

CSecureChannelClient  *pSCClient;
IWMDMStorage  *pStorgae;

HMAC  hMAC;
BYTE  abMAC[WMDM_MAC_LENGTH];
BYTE  abMACVerify[WMDM_MAC_LENGTH];

hr = pStorage->GetRights(&pRights, &nRightsCount, abMAC);
if (SUCCEEDED(hr))
{
    //
    // First verify the integrity of the retrieved rights.
    //
    pSCClient->MACInit(&hMAC);
    pSCClient->MACUpdate(hMAC, (BYTE*)(pRights), 
                    sizeof(WMDMRIGHTS) * nRightsCount);
    pSCClient->MACUpdate(hMAC, (BYTE*)(&nRightsCount), 
                                 sizeof(nRightsCount));
    pSCClient->MACFinal(hMAC, (BYTE*)abMACVerify);
    if (memcmp(abMACVerify, abMAC, sizeof(abMAC)) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
    }
}


```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a>



<a href="/windows/desktop/WMDM/wmdmrights">WMDMRIGHTS</a>