---
UID: NF:mswmdm.IMDSPStorage.GetName
title: IMDSPStorage::GetName (mswmdm.h)
description: The GetName method retrieves the display name of the storage object.
helpviewer_keywords: ["GetName","GetName method [windows Media Device Manager]","GetName method [windows Media Device Manager]","IMDSPStorage interface","IMDSPStorage interface [windows Media Device Manager]","GetName method","IMDSPStorage.GetName","IMDSPStorage::GetName","IMDSPStorageGetName","mswmdm/IMDSPStorage::GetName","wmdm.imdspstorage_getname"]
old-location: wmdm\imdspstorage_getname.htm
tech.root: WMDM
ms.assetid: 6172f222-8b92-4da5-8001-b79431c26518
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [windows Media Device Manager], GetName method [windows Media Device Manager],IMDSPStorage interface, IMDSPStorage interface [windows Media Device Manager],GetName method, IMDSPStorage.GetName, IMDSPStorage::GetName, IMDSPStorageGetName, mswmdm/IMDSPStorage::GetName, wmdm.imdspstorage_getname
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
 - IMDSPStorage::GetName
 - mswmdm/IMDSPStorage::GetName
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
 - IMDSPStorage.GetName
---

# IMDSPStorage::GetName


## -description

The <b>GetName</b> method retrieves the display name of the storage object.

## -parameters

### -param pwszName [out]

Pointer to a (Unicode) wide-character null-terminated string containing the object name.

### -param nMaxChars [in]

Integer containing the maximum number of characters that can be copied to the name string.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The display name of the object is the file name without path information. In hierarchical media the display name would be concatenated with the ancestor instances of <b>IMDSPStorage</b> interfaces to create a full path-qualified name.

The <b>LPWSTR</b> string type is a 16-bit Unicode character string and does not accept byte-sized characters.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate">IMDSPStorage::GetDate</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getsize">IMDSPStorage::GetSize</a>