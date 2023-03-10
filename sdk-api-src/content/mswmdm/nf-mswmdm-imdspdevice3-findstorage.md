---
UID: NF:mswmdm.IMDSPDevice3.FindStorage
title: IMDSPDevice3::FindStorage (mswmdm.h)
description: The FindStorage method finds a storage with the given persistent unique identifier. The persistent unique identifier of a storage is described by the g_wszWMDMPersistentUniqueID property of that storage. (IMDSPDevice3.FindStorage)
helpviewer_keywords: ["FindStorage","FindStorage method [windows Media Device Manager]","FindStorage method [windows Media Device Manager]","IMDSPDevice3 interface","IMDSPDevice3 interface [windows Media Device Manager]","FindStorage method","IMDSPDevice3.FindStorage","IMDSPDevice3::FindStorage","IMDSPDevice3FindStorage","mswmdm/IMDSPDevice3::FindStorage","wmdm.imdspdevice3_findstorage"]
old-location: wmdm\imdspdevice3_findstorage.htm
tech.root: WMDM
ms.assetid: d80812fc-750a-41f3-ba00-695e168259c0
ms.date: 12/05/2018
ms.keywords: FindStorage, FindStorage method [windows Media Device Manager], FindStorage method [windows Media Device Manager],IMDSPDevice3 interface, IMDSPDevice3 interface [windows Media Device Manager],FindStorage method, IMDSPDevice3.FindStorage, IMDSPDevice3::FindStorage, IMDSPDevice3FindStorage, mswmdm/IMDSPDevice3::FindStorage, wmdm.imdspdevice3_findstorage
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
 - IMDSPDevice3::FindStorage
 - mswmdm/IMDSPDevice3::FindStorage
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
 - IMDSPDevice3.FindStorage
---

# IMDSPDevice3::FindStorage


## -description

The <b>FindStorage</b> method finds a storage with the given persistent unique identifier. The persistent unique identifier of a storage is described by the <b>g_wszWMDMPersistentUniqueID</b> property of that storage.

## -parameters

### -param findScope [in]

Scope of the find operation. It must be one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_FIND_SCOPE_GLOBAL</td>
<td>Search the whole device.</td>
</tr>
<tr>
<td>WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN</td>
<td>Search only in the immediate children of the current storage.</td>
</tr>
</table>

### -param pwszUniqueID [in]

Persistent unique identifier of the storage.

### -param ppStorage [out]

Pointer to the returned storage specified by the <i>pwszUniqueID</i> parameter.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The service provider returns a persistent unique identifier through the <b>g_wszWMDMPersistentUniqueID</b> property of the storage. For a specific storage, the persistent unique identifier supplied by service provider should be same across different device connect sessions.

The application may call <b>FindStorage</b> with this persistent unique identifier at a later point. In response, Windows Media Device Manager calls this method on the service provider (SP).

A persistent unique identifier is used to uniquely identify content stored on a particular device. It does not represent a content-specific globally unique identifier that remains identical across all devices. Thus, the same content stored in different storages will have different persistent unique identifiers.

Windows Media Device Manager calls this method only for devices that are registered to enable synchronization with Windows Media Player. For more information, see <a href="/windows/desktop/WMDM/enabling-synchronization-with-windows-media-player">Enabling Synchronization with Windows Media Player</a>.

## -see-also

<a href="/windows/desktop/WMDM/enabling-synchronization-with-windows-media-player">Enabling Synchronization with Windows Media Player</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3">IMDSPDevice3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage3-getmetadata">IMDSPStorage3::GetMetadata</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage4-findstorage">IMDSPStorage4::FindStorage</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage4-getspecifiedmetadata">IMDSPStorage4::GetSpecifiedMetadata</a>



<a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>



<a href="/windows/desktop/WMDM/wmdm-find-scope">WMDM_FIND_SCOPE</a>
