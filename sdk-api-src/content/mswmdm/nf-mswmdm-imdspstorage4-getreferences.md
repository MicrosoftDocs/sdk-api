---
UID: NF:mswmdm.IMDSPStorage4.GetReferences
title: IMDSPStorage4::GetReferences (mswmdm.h)
description: The GetReferences method returns an array of pointers to IMDSPStorage objects comprising the references contained in an association storage, such as one representing playlist or album objects.
helpviewer_keywords: ["GetReferences","GetReferences method [windows Media Device Manager]","GetReferences method [windows Media Device Manager]","IMDSPStorage4 interface","IMDSPStorage4 interface [windows Media Device Manager]","GetReferences method","IMDSPStorage4.GetReferences","IMDSPStorage4::GetReferences","IMDSPStorage4GetReferences","mswmdm/IMDSPStorage4::GetReferences","wmdm.imdspstorage4_getreferences"]
old-location: wmdm\imdspstorage4_getreferences.htm
tech.root: WMDM
ms.assetid: f8caf10b-69d4-4d37-836e-af260840254f
ms.date: 12/05/2018
ms.keywords: GetReferences, GetReferences method [windows Media Device Manager], GetReferences method [windows Media Device Manager],IMDSPStorage4 interface, IMDSPStorage4 interface [windows Media Device Manager],GetReferences method, IMDSPStorage4.GetReferences, IMDSPStorage4::GetReferences, IMDSPStorage4GetReferences, mswmdm/IMDSPStorage4::GetReferences, wmdm.imdspstorage4_getreferences
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
 - IMDSPStorage4::GetReferences
 - mswmdm/IMDSPStorage4::GetReferences
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
 - IMDSPStorage4.GetReferences
---

# IMDSPStorage4::GetReferences


## -description

The <b>GetReferences</b> method returns an array of pointers to <b>IMDSPStorage</b> objects comprising the references contained in an association storage, such as one representing playlist or album objects.

## -parameters

### -param pdwRefs [out]

Pointer to the count of <b>IWMDMStorage</b> interface pointers being returned in <i>pppIWMDMStorage</i>.

### -param pppISPStorage [out]

Pointer to a pointer to the array of <b>IWMDMStorage</b> interface pointers that represent references on a storage. Such references can, for example, represent items in a playlist or album. The ordering of references matches the ordering in this array. Memory for this array should be allocated by the service provider.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Windows Media Device Manager uses this method for obtaining the references on an association storage such as a playlist or an album.

If the storage has references to one or more items that have been deleted from the device, the SP should not include these references in the references returned. The SP should indicate such condition by returning S_FALSE. The application might choose to refresh the association storage object by using the known-good references returned here. The SP can also refresh the references itself.

If the count of references is 0, service provider must return an array of references with 0 elements in it.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4">IMDSPStorage4 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage4-setreferences">IMDSPStorage4::SetReferences</a>