---
UID: NF:mswmdm.IMDSPDevice2.GetStorage
title: IMDSPDevice2::GetStorage (mswmdm.h)
description: The GetStorage method makes it possible to go directly to a storage based on its name instead of enumerating through all storages to find it.
helpviewer_keywords: ["GetStorage","GetStorage method [windows Media Device Manager]","GetStorage method [windows Media Device Manager]","IMDSPDevice2 interface","IMDSPDevice2 interface [windows Media Device Manager]","GetStorage method","IMDSPDevice2.GetStorage","IMDSPDevice2::GetStorage","IMDSPDevice2GetStorage","mswmdm/IMDSPDevice2::GetStorage","wmdm.imdspdevice2_getstorage"]
old-location: wmdm\imdspdevice2_getstorage.htm
tech.root: WMDM
ms.assetid: d01cf5a6-1fdb-4354-8b43-b04bdc562d71
ms.date: 12/05/2018
ms.keywords: GetStorage, GetStorage method [windows Media Device Manager], GetStorage method [windows Media Device Manager],IMDSPDevice2 interface, IMDSPDevice2 interface [windows Media Device Manager],GetStorage method, IMDSPDevice2.GetStorage, IMDSPDevice2::GetStorage, IMDSPDevice2GetStorage, mswmdm/IMDSPDevice2::GetStorage, wmdm.imdspdevice2_getstorage
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
 - IMDSPDevice2::GetStorage
 - mswmdm/IMDSPDevice2::GetStorage
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
 - IMDSPDevice2.GetStorage
---

# IMDSPDevice2::GetStorage


## -description

The <b>GetStorage</b> method makes it possible to go directly to a storage based on its name instead of enumerating through all storages to find it.

## -parameters

### -param pszStorageName [in]

Pointer to a null-terminated string containing the name of the storage to find.

### -param ppStorage [out]

Pointer to the storage object specified by the <i>pszStorageName</i> parameter.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The <b>GetStorage</b> method does not support wildcard characters. It is not recursive, that is, it will only find storages in the root of the device.

If this method is not implemented, it should return E_NOTIMPL. (It should not return WMDM_E_NOT_SUPPORTED or any other codes indicating that this method is not implemented). This will ensure that Windows Media Device Manager will attempt to substitute this functionality itself by enumerating all storages to find a match based on the storage name passed in as <i>pszStorageName</i>.

It is strongly recommended that a service provider implement this method to efficiently return a storage object based on name.

This method is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2">IMDSPDevice2 Interface</a>