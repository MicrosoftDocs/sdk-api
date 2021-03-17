---
UID: NF:mswmdm.IMDSPStorage.EnumStorage
title: IMDSPStorage::EnumStorage (mswmdm.h)
description: The EnumStorage method accesses the IMDSPEnumStorage interface to enumerate the individual storage media on a device.
helpviewer_keywords: ["EnumStorage","EnumStorage method [windows Media Device Manager]","EnumStorage method [windows Media Device Manager]","IMDSPStorage interface","IMDSPStorage interface [windows Media Device Manager]","EnumStorage method","IMDSPStorage.EnumStorage","IMDSPStorage::EnumStorage","IMDSPStorageEnumStorage","mswmdm/IMDSPStorage::EnumStorage","wmdm.imdspstorage_enumstorage"]
old-location: wmdm\imdspstorage_enumstorage.htm
tech.root: WMDM
ms.assetid: 8b97d023-172f-4335-8d15-e5a4b67f24b8
ms.date: 12/05/2018
ms.keywords: EnumStorage, EnumStorage method [windows Media Device Manager], EnumStorage method [windows Media Device Manager],IMDSPStorage interface, IMDSPStorage interface [windows Media Device Manager],EnumStorage method, IMDSPStorage.EnumStorage, IMDSPStorage::EnumStorage, IMDSPStorageEnumStorage, mswmdm/IMDSPStorage::EnumStorage, wmdm.imdspstorage_enumstorage
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
 - IMDSPStorage::EnumStorage
 - mswmdm/IMDSPStorage::EnumStorage
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
 - IMDSPStorage.EnumStorage
---

# IMDSPStorage::EnumStorage


## -description

The <b>EnumStorage</b> method accesses the <b>IMDSPEnumStorage</b> interface to enumerate the individual storage media on a device.

## -parameters

### -param ppEnumStorage [out]

Pointer to an <b>IMDSPEnumStorage</b> interface.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The <b>IMDSPEnumStorage</b> interface returned will enumerate the nested storages in the storage that <b>IMDSPStorage</b> corresponds to. Thus all the storage objects in a hierarchical structure can be retrieved recursively.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-enumstorage">IMDSPDevice::EnumStorage</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage">IMDSPEnumStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>