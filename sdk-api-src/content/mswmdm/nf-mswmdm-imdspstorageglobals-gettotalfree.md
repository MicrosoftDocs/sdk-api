---
UID: NF:mswmdm.IMDSPStorageGlobals.GetTotalFree
title: IMDSPStorageGlobals::GetTotalFree (mswmdm.h)
description: The GetTotalFree method retrieves the total free space on the storage medium, in bytes.
helpviewer_keywords: ["GetTotalFree","GetTotalFree method [windows Media Device Manager]","GetTotalFree method [windows Media Device Manager]","IMDSPStorageGlobals interface","IMDSPStorageGlobals interface [windows Media Device Manager]","GetTotalFree method","IMDSPStorageGlobals.GetTotalFree","IMDSPStorageGlobals::GetTotalFree","IMDSPStorageGlobalsGetTotalFree","mswmdm/IMDSPStorageGlobals::GetTotalFree","wmdm.imdspstorageglobals_gettotalfree"]
old-location: wmdm\imdspstorageglobals_gettotalfree.htm
tech.root: WMDM
ms.assetid: 141b33e8-5cb5-46a8-b91e-01bd9c634cbf
ms.date: 12/05/2018
ms.keywords: GetTotalFree, GetTotalFree method [windows Media Device Manager], GetTotalFree method [windows Media Device Manager],IMDSPStorageGlobals interface, IMDSPStorageGlobals interface [windows Media Device Manager],GetTotalFree method, IMDSPStorageGlobals.GetTotalFree, IMDSPStorageGlobals::GetTotalFree, IMDSPStorageGlobalsGetTotalFree, mswmdm/IMDSPStorageGlobals::GetTotalFree, wmdm.imdspstorageglobals_gettotalfree
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
 - IMDSPStorageGlobals::GetTotalFree
 - mswmdm/IMDSPStorageGlobals::GetTotalFree
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
 - IMDSPStorageGlobals.GetTotalFree
---

# IMDSPStorageGlobals::GetTotalFree


## -description

The <b>GetTotalFree</b> method retrieves the total free space on the storage medium, in bytes.

## -parameters

### -param pdwFreeLow [out]

Pointer to a <b>DWORD</b> containing the low-order bytes of the free space.

### -param pdwFreeHigh [out]

Pointer to a <b>DWORD</b> containing the high-order bytes of the free space.

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



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-gettotalsize">IMDSPStorageGlobals::GetTotalSize</a>