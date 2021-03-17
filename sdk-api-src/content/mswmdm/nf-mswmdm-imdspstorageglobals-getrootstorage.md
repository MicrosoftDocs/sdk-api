---
UID: NF:mswmdm.IMDSPStorageGlobals.GetRootStorage
title: IMDSPStorageGlobals::GetRootStorage (mswmdm.h)
description: The GetRootStorage method retrieves a pointer to the IMDSPStorage interface for the root storage of the storage medium.
helpviewer_keywords: ["GetRootStorage","GetRootStorage method [windows Media Device Manager]","GetRootStorage method [windows Media Device Manager]","IMDSPStorageGlobals interface","IMDSPStorageGlobals interface [windows Media Device Manager]","GetRootStorage method","IMDSPStorageGlobals.GetRootStorage","IMDSPStorageGlobals::GetRootStorage","IMDSPStorageGlobalsGetRootStorage","mswmdm/IMDSPStorageGlobals::GetRootStorage","wmdm.imdspstorageglobals_getrootstorage"]
old-location: wmdm\imdspstorageglobals_getrootstorage.htm
tech.root: WMDM
ms.assetid: 80b6cb71-d567-4fb5-9f75-82ae2fe118c7
ms.date: 12/05/2018
ms.keywords: GetRootStorage, GetRootStorage method [windows Media Device Manager], GetRootStorage method [windows Media Device Manager],IMDSPStorageGlobals interface, IMDSPStorageGlobals interface [windows Media Device Manager],GetRootStorage method, IMDSPStorageGlobals.GetRootStorage, IMDSPStorageGlobals::GetRootStorage, IMDSPStorageGlobalsGetRootStorage, mswmdm/IMDSPStorageGlobals::GetRootStorage, wmdm.imdspstorageglobals_getrootstorage
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
 - IMDSPStorageGlobals::GetRootStorage
 - mswmdm/IMDSPStorageGlobals::GetRootStorage
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
 - IMDSPStorageGlobals.GetRootStorage
---

# IMDSPStorageGlobals::GetRootStorage


## -description

The <b>GetRootStorage</b> method retrieves a pointer to the <b>IMDSPStorage</b> interface for the root storage of the storage medium.

## -parameters

### -param ppRoot [out]

Pointer to an <b>IMDSPStorage</b> pointer that receives the root storage.

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

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals">IMDSPStorageGlobals Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>