---
UID: NF:mswmdm.IMDSPStorageGlobals.GetTotalBad
title: IMDSPStorageGlobals::GetTotalBad (mswmdm.h)
description: The GetTotalBad method retrieves the total amount of unusable space on the storage medium, in bytes. (IMDSPStorageGlobals.GetTotalBad)
helpviewer_keywords: ["GetTotalBad","GetTotalBad method [windows Media Device Manager]","GetTotalBad method [windows Media Device Manager]","IMDSPStorageGlobals interface","IMDSPStorageGlobals interface [windows Media Device Manager]","GetTotalBad method","IMDSPStorageGlobals.GetTotalBad","IMDSPStorageGlobals::GetTotalBad","IMDSPStorageGlobalsGetTotalBad","mswmdm/IMDSPStorageGlobals::GetTotalBad","wmdm.imdspstorageglobals_gettotalbad"]
old-location: wmdm\imdspstorageglobals_gettotalbad.htm
tech.root: WMDM
ms.assetid: b0cbf636-e2c4-4a30-9b6d-5833090330a4
ms.date: 12/05/2018
ms.keywords: GetTotalBad, GetTotalBad method [windows Media Device Manager], GetTotalBad method [windows Media Device Manager],IMDSPStorageGlobals interface, IMDSPStorageGlobals interface [windows Media Device Manager],GetTotalBad method, IMDSPStorageGlobals.GetTotalBad, IMDSPStorageGlobals::GetTotalBad, IMDSPStorageGlobalsGetTotalBad, mswmdm/IMDSPStorageGlobals::GetTotalBad, wmdm.imdspstorageglobals_gettotalbad
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
 - IMDSPStorageGlobals::GetTotalBad
 - mswmdm/IMDSPStorageGlobals::GetTotalBad
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
 - IMDSPStorageGlobals.GetTotalBad
---

# IMDSPStorageGlobals::GetTotalBad


## -description

The <b>GetTotalBad</b> method retrieves the total amount of unusable space on the storage medium, in bytes.

## -parameters

### -param pdwBadLow [out]

Pointer to a <b>DWORD</b> containing the low-order bytes of the unusable space.

### -param pdwBadHigh [out]

Pointer to a <b>DWORD</b> containing the high-order bytes of the unusable space.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

To determine the amount of storage space in use by the medium for file management, subtract the number of bad bytes identified by using <b>GetTotalBad</b> from the number of free bytes identified by using <b>GetTotalFree</b>.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals">IMDSPStorageGlobals Interface</a>
