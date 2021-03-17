---
UID: NF:mswmdm.IMDSPStorage.GetStorageGlobals
title: IMDSPStorage::GetStorageGlobals (mswmdm.h)
description: The GetStorageGlobals method retrieves the IMDSPStorageGlobals interface to provide access to global information about a storage medium.
helpviewer_keywords: ["GetStorageGlobals","GetStorageGlobals method [windows Media Device Manager]","GetStorageGlobals method [windows Media Device Manager]","IMDSPStorage interface","IMDSPStorage interface [windows Media Device Manager]","GetStorageGlobals method","IMDSPStorage.GetStorageGlobals","IMDSPStorage::GetStorageGlobals","IMDSPStorageGetStorageGlobals","mswmdm/IMDSPStorage::GetStorageGlobals","wmdm.imdspstorage_getstorageglobals"]
old-location: wmdm\imdspstorage_getstorageglobals.htm
tech.root: WMDM
ms.assetid: 93c963ea-9b00-4897-838c-fdc06c781a2d
ms.date: 12/05/2018
ms.keywords: GetStorageGlobals, GetStorageGlobals method [windows Media Device Manager], GetStorageGlobals method [windows Media Device Manager],IMDSPStorage interface, IMDSPStorage interface [windows Media Device Manager],GetStorageGlobals method, IMDSPStorage.GetStorageGlobals, IMDSPStorage::GetStorageGlobals, IMDSPStorageGetStorageGlobals, mswmdm/IMDSPStorage::GetStorageGlobals, wmdm.imdspstorage_getstorageglobals
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
 - IMDSPStorage::GetStorageGlobals
 - mswmdm/IMDSPStorage::GetStorageGlobals
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
 - IMDSPStorage.GetStorageGlobals
---

# IMDSPStorage::GetStorageGlobals


## -description

The <b>GetStorageGlobals</b> method retrieves the <b>IMDSPStorageGlobals</b> interface to provide access to global information about a storage medium.

## -parameters

### -param ppStorageGlobals [out]

Pointer to an <b>IMDSPStorageGlobals</b> interface that can provide access to global information about a storage medium.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The <b>IMDSPStorageGlobals</b> interface provides methods for accessing global information about the medium regardless of the nesting level of the <b>IMDSPStorage</b> interface from which the global view is accessed. Any instance of <b>IMDSPStorage</b> can acquire an <b>IMDSPStorageGlobals</b> interface.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals">IMDSPStorageGlobals Interface</a>