---
UID: NF:mswmdm.IMDSPStorage4.SetReferences
title: IMDSPStorage4::SetReferences (mswmdm.h)
description: The SetReferences method sets the references contained in a storage that has references (such as playlist/album), overwriting any previously existing references contained in this storage.
helpviewer_keywords: ["IMDSPStorage4 interface [windows Media Device Manager]","SetReferences method","IMDSPStorage4.SetReferences","IMDSPStorage4::SetReferences","IMDSPStorage4SetReferences","SetReferences","SetReferences method [windows Media Device Manager]","SetReferences method [windows Media Device Manager]","IMDSPStorage4 interface","mswmdm/IMDSPStorage4::SetReferences","wmdm.imdspstorage4_setreferences"]
old-location: wmdm\imdspstorage4_setreferences.htm
tech.root: WMDM
ms.assetid: 45fd9efa-b03d-46de-9d8c-85ed04d446dd
ms.date: 12/05/2018
ms.keywords: IMDSPStorage4 interface [windows Media Device Manager],SetReferences method, IMDSPStorage4.SetReferences, IMDSPStorage4::SetReferences, IMDSPStorage4SetReferences, SetReferences, SetReferences method [windows Media Device Manager], SetReferences method [windows Media Device Manager],IMDSPStorage4 interface, mswmdm/IMDSPStorage4::SetReferences, wmdm.imdspstorage4_setreferences
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
 - IMDSPStorage4::SetReferences
 - mswmdm/IMDSPStorage4::SetReferences
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
 - IMDSPStorage4.SetReferences
---

# IMDSPStorage4::SetReferences


## -description

The <b>SetReferences</b> method sets the references contained in a storage that has references (such as playlist/album), overwriting any previously existing references contained in this storage.

## -parameters

### -param dwRefs [in]

Count of <b>IMDSPStorage</b> interface pointers contained in the passed-in array. Zero is an acceptable value and resets the storage to contain zero references. The storage itself is not deleted in this case.

### -param ppISPStorage [in]

Pointer to an array of <b>IMDSPStorage</b> interface pointers used to set references in a storage. The ordering of references matches the ordering of the corresponding <b>IWMDMStorage</b> interface pointers in this array. <b>NULL</b> is an acceptable value if <i>dwRefs</i> is also zero.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Any valid <b>IMDSPStorage</b> object may be contained in the <i>ppIMDSPStorage</i> array. This includes folders and other storages containing references themselves (creating, for example, a playlist of playlists).

Depending upon the level of support in the device (whether it supports playlists or nested playlists), the service provider should handle this method appropriately. If the device does not have the level of supported needed for the passed-in reference array, the service provider should return WMDM_E_NOTSUPPORTED.

If the reference contains a deleted storage, WMDM_E_INTERFACEDEAD should be returned.

The <b>SetReferences</b> method follows a wipe-and-load model. The references passed include a complete set and should replace any existing references on the storage object completely.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4">IMDSPStorage4 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage4-getreferences">IMDSPStorage4::GetReferences</a>