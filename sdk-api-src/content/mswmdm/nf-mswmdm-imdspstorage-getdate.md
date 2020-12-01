---
UID: NF:mswmdm.IMDSPStorage.GetDate
title: IMDSPStorage::GetDate (mswmdm.h)
description: The GetDate method retrieves the date on which the storage object (file or folder) was most recently modified.
helpviewer_keywords: ["GetDate","GetDate method [windows Media Device Manager]","GetDate method [windows Media Device Manager]","IMDSPStorage interface","IMDSPStorage interface [windows Media Device Manager]","GetDate method","IMDSPStorage.GetDate","IMDSPStorage::GetDate","IMDSPStorageGetDate","mswmdm/IMDSPStorage::GetDate","wmdm.imdspstorage_getdate"]
old-location: wmdm\imdspstorage_getdate.htm
tech.root: WMDM
ms.assetid: 4ba0c598-9ea2-42cc-a234-1c0e192971a8
ms.date: 12/05/2018
ms.keywords: GetDate, GetDate method [windows Media Device Manager], GetDate method [windows Media Device Manager],IMDSPStorage interface, IMDSPStorage interface [windows Media Device Manager],GetDate method, IMDSPStorage.GetDate, IMDSPStorage::GetDate, IMDSPStorageGetDate, mswmdm/IMDSPStorage::GetDate, wmdm.imdspstorage_getdate
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
 - IMDSPStorage::GetDate
 - mswmdm/IMDSPStorage::GetDate
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
 - IMDSPStorage.GetDate
---

# IMDSPStorage::GetDate


## -description

The <b>GetDate</b> method retrieves the date on which the storage object (file or folder) was most recently modified.

## -parameters

### -param pDateTimeUTC [out]

Pointer to a <b>WMDMDATETIME</b> structure containing the date on which the file or folder was most recently modified.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The time is specified in coordinated universal time.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getname">IMDSPStorage::GetName</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getsize">IMDSPStorage::GetSize</a>



<a href="/windows/desktop/WMDM/wmdmdatetime">WMDMDATETIME</a>