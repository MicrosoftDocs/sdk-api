---
UID: NF:mswmdm.IMDSPStorage.SetAttributes
title: IMDSPStorage::SetAttributes (mswmdm.h)
description: The SetAttributes method sets the attributes of a storage object.
helpviewer_keywords: ["IMDSPStorage interface [windows Media Device Manager]","SetAttributes method","IMDSPStorage.SetAttributes","IMDSPStorage::SetAttributes","IMDSPStorageSetAttributes","SetAttributes","SetAttributes method [windows Media Device Manager]","SetAttributes method [windows Media Device Manager]","IMDSPStorage interface","mswmdm/IMDSPStorage::SetAttributes","wmdm.imdspstorage_setattributes"]
old-location: wmdm\imdspstorage_setattributes.htm
tech.root: WMDM
ms.assetid: e995b255-364f-4ea6-b7fd-4443e84432ef
ms.date: 12/05/2018
ms.keywords: IMDSPStorage interface [windows Media Device Manager],SetAttributes method, IMDSPStorage.SetAttributes, IMDSPStorage::SetAttributes, IMDSPStorageSetAttributes, SetAttributes, SetAttributes method [windows Media Device Manager], SetAttributes method [windows Media Device Manager],IMDSPStorage interface, mswmdm/IMDSPStorage::SetAttributes, wmdm.imdspstorage_setattributes
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
 - IMDSPStorage::SetAttributes
 - mswmdm/IMDSPStorage::SetAttributes
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
 - IMDSPStorage.SetAttributes
---

# IMDSPStorage::SetAttributes


## -description

The <b>SetAttributes</b> method sets the attributes of a storage object.

## -parameters

### -param dwAttributes [in]

<b>DWORD</b> containing the attributes to be set as defined in the <b>IWMDMStorage::SetAttributes</b> method.

### -param pFormat [in]

Pointer to a <b>_WAVEFORMATEX</b> structure that contains attribute information about the object. This parameter is optional and is ignored if the file is not audio.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Many of the attributes returned by <b>GetAttributes</b> (as listed in attribute table for <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes">IWMDMStorage::GetAttributes</a>) cannot be set, so they are not listed in the attribute table for <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes">IWMDMStorage::SetAttributes</a>.

This method is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage">IMDSPEnumStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage2-setattributes2">IMDSPStorage2::SetAttributes2</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes">IMDSPStorage::GetAttributes</a>



<a href="/windows/desktop/WMDM/-waveformatex">_WAVEFORMATEX</a>