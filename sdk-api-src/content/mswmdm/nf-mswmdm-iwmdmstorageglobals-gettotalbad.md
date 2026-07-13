---
UID: NF:mswmdm.IWMDMStorageGlobals.GetTotalBad
title: IWMDMStorageGlobals::GetTotalBad (mswmdm.h)
description: The GetTotalBad method retrieves the total amount of unusable space on the storage medium, in bytes. (IWMDMStorageGlobals.GetTotalBad)
helpviewer_keywords: ["GetTotalBad","GetTotalBad method [windows Media Device Manager]","GetTotalBad method [windows Media Device Manager]","IWMDMStorageGlobals interface","IWMDMStorageGlobals interface [windows Media Device Manager]","GetTotalBad method","IWMDMStorageGlobals.GetTotalBad","IWMDMStorageGlobals::GetTotalBad","IWMDMStorageGlobalsGetTotalBad","mswmdm/IWMDMStorageGlobals::GetTotalBad","wmdm.iwmdmstorageglobals_gettotalbad"]
old-location: wmdm\iwmdmstorageglobals_gettotalbad.htm
tech.root: WMDM
ms.assetid: 40e1a39b-2757-472c-b585-77b829605e8c
ms.date: 12/05/2018
ms.keywords: GetTotalBad, GetTotalBad method [windows Media Device Manager], GetTotalBad method [windows Media Device Manager],IWMDMStorageGlobals interface, IWMDMStorageGlobals interface [windows Media Device Manager],GetTotalBad method, IWMDMStorageGlobals.GetTotalBad, IWMDMStorageGlobals::GetTotalBad, IWMDMStorageGlobalsGetTotalBad, mswmdm/IWMDMStorageGlobals::GetTotalBad, wmdm.iwmdmstorageglobals_gettotalbad
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
 - IWMDMStorageGlobals::GetTotalBad
 - mswmdm/IWMDMStorageGlobals::GetTotalBad
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
 - IWMDMStorageGlobals.GetTotalBad
---

# IWMDMStorageGlobals::GetTotalBad


## -description

The <b>GetTotalBad</b> method retrieves the total amount of unusable space on the storage medium, in bytes.

## -parameters

### -param pdwBadLow [out]

Pointer to a <b>DWORD</b> that receives the low-order bytes of unusable space.

### -param pdwBadHigh [out]

Pointer to a <b>DWORD</b> that receives the high-order bytes of unusable space.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

To determine the amount of storage space in use by the medium for file management, subtract the number of bad bytes retrieved using <b>GetTotalBad</b> from the number of free bytes retrieved using <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-gettotalfree">GetTotalFree</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-gettotalfree">IWMDMStorageGlobals::GetTotalFree</a>
