---
UID: NF:mswmdm.IMDSPEnumStorage.Next
title: IMDSPEnumStorage::Next (mswmdm.h)
description: The Next method returns a pointer to the next celtIMDSPStorage interfaces.
helpviewer_keywords: ["IMDSPEnumStorage interface [windows Media Device Manager]","Next method","IMDSPEnumStorage.Next","IMDSPEnumStorage::Next","IMDSPEnumStorageNext","Next","Next method [windows Media Device Manager]","Next method [windows Media Device Manager]","IMDSPEnumStorage interface","mswmdm/IMDSPEnumStorage::Next","wmdm.imdspenumstorage_next"]
old-location: wmdm\imdspenumstorage_next.htm
tech.root: WMDM
ms.assetid: 7874912a-6350-445c-a7c8-0f885d756aa0
ms.date: 12/05/2018
ms.keywords: IMDSPEnumStorage interface [windows Media Device Manager],Next method, IMDSPEnumStorage.Next, IMDSPEnumStorage::Next, IMDSPEnumStorageNext, Next, Next method [windows Media Device Manager], Next method [windows Media Device Manager],IMDSPEnumStorage interface, mswmdm/IMDSPEnumStorage::Next, wmdm.imdspenumstorage_next
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
 - IMDSPEnumStorage::Next
 - mswmdm/IMDSPEnumStorage::Next
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
 - IMDSPEnumStorage.Next
---

# IMDSPEnumStorage::Next


## -description

The <b>Next</b> method returns a pointer to the next <i>celt</i><a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage</a> interfaces.

## -parameters

### -param celt [in]

Number of storage interfaces requested.

### -param ppStorage [out]

Array of <i>celt</i><a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage</a> interface pointers allocated by the caller. Return <b>NULL</b> if no more storage media exist, or an error has occurred. If <i>celt</i> is more than 1, the caller must allocate enough memory to store <i>celt</i> number of interface pointers.

### -param pceltFetched [out]

Pointer to a <b>ULONG</b> variable that receives the count of interfaces returned.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

When there are no more storage interfaces, or when there are fewer storage interfaces than requested, the return value from <b>Next</b> is S_FALSE. When this happens, the <i>pceltFetched</i> parameter must be queried to determine how many interfaces, if any, were returned.

The storage enumerator may not reflect the effect of media insertion and removal. In such cases, the client should obtain a new enumerator object.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage">IMDSPEnumStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>