---
UID: NF:mswmdm.IMDSPStorageGlobals.GetTotalSize
title: IMDSPStorageGlobals::GetTotalSize (mswmdm.h)
description: The GetTotalSize method retrieves the total size, in bytes, of the medium associated with this IMDSPStorageGlobals interface.
helpviewer_keywords: ["GetTotalSize","GetTotalSize method [windows Media Device Manager]","GetTotalSize method [windows Media Device Manager]","IMDSPStorageGlobals interface","IMDSPStorageGlobals interface [windows Media Device Manager]","GetTotalSize method","IMDSPStorageGlobals.GetTotalSize","IMDSPStorageGlobals::GetTotalSize","IMDSPStorageGlobalsGetTotalSize","mswmdm/IMDSPStorageGlobals::GetTotalSize","wmdm.imdspstorageglobals_gettotalsize"]
old-location: wmdm\imdspstorageglobals_gettotalsize.htm
tech.root: WMDM
ms.assetid: 6a4b4ac5-0b7e-4a22-9857-b251a6bf1dcf
ms.date: 12/05/2018
ms.keywords: GetTotalSize, GetTotalSize method [windows Media Device Manager], GetTotalSize method [windows Media Device Manager],IMDSPStorageGlobals interface, IMDSPStorageGlobals interface [windows Media Device Manager],GetTotalSize method, IMDSPStorageGlobals.GetTotalSize, IMDSPStorageGlobals::GetTotalSize, IMDSPStorageGlobalsGetTotalSize, mswmdm/IMDSPStorageGlobals::GetTotalSize, wmdm.imdspstorageglobals_gettotalsize
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
 - IMDSPStorageGlobals::GetTotalSize
 - mswmdm/IMDSPStorageGlobals::GetTotalSize
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
 - IMDSPStorageGlobals.GetTotalSize
---

# IMDSPStorageGlobals::GetTotalSize


## -description

The <b>GetTotalSize</b> method retrieves the total size, in bytes, of the medium associated with this <b>IMDSPStorageGlobals</b> interface.

## -parameters

### -param pdwTotalSizeLow [out]

Pointer to a <b>DWORD</b> containing the low-order bytes of the total size of the medium.

### -param pdwTotalSizeHigh [out]

Pointer to a <b>DWORD</b> containing the high-order bytes of the total size of the medium.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals">IMDSPStorageGlobals Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-gettotalfree">IMDSPStorageGlobals::GetTotalFree</a>