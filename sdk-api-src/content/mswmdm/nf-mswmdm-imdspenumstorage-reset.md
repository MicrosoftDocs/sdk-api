---
UID: NF:mswmdm.IMDSPEnumStorage.Reset
title: IMDSPEnumStorage::Reset (mswmdm.h)
description: The Reset method resets the enumeration sequence to the beginning. A subsequent call to the Next method fetches the first storage interface in the enumeration sequence.
helpviewer_keywords: ["IMDSPEnumStorage interface [windows Media Device Manager]","Reset method","IMDSPEnumStorage.Reset","IMDSPEnumStorage::Reset","IMDSPEnumStorageReset","Reset","Reset method [windows Media Device Manager]","Reset method [windows Media Device Manager]","IMDSPEnumStorage interface","mswmdm/IMDSPEnumStorage::Reset","wmdm.imdspenumstorage_reset"]
old-location: wmdm\imdspenumstorage_reset.htm
tech.root: WMDM
ms.assetid: 1296406c-2c5d-4db8-965e-db11a9759560
ms.date: 12/05/2018
ms.keywords: IMDSPEnumStorage interface [windows Media Device Manager],Reset method, IMDSPEnumStorage.Reset, IMDSPEnumStorage::Reset, IMDSPEnumStorageReset, Reset, Reset method [windows Media Device Manager], Reset method [windows Media Device Manager],IMDSPEnumStorage interface, mswmdm/IMDSPEnumStorage::Reset, wmdm.imdspenumstorage_reset
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
 - IMDSPEnumStorage::Reset
 - mswmdm/IMDSPEnumStorage::Reset
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
 - IMDSPEnumStorage.Reset
---

# IMDSPEnumStorage::Reset


## -description

The <b>Reset</b> method resets the enumeration sequence to the beginning. A subsequent call to the <b>Next</b> method fetches the first storage interface in the enumeration sequence.



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

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage">IMDSPEnumStorage Interface</a>
