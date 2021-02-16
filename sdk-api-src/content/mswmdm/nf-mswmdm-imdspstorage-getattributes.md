---
UID: NF:mswmdm.IMDSPStorage.GetAttributes
title: IMDSPStorage::GetAttributes (mswmdm.h)
description: The GetAttributes method retrieves the attributes of this storage object.
helpviewer_keywords: ["GetAttributes","GetAttributes method [windows Media Device Manager]","GetAttributes method [windows Media Device Manager]","IMDSPStorage interface","IMDSPStorage interface [windows Media Device Manager]","GetAttributes method","IMDSPStorage.GetAttributes","IMDSPStorage::GetAttributes","IMDSPStorageGetAttributes","mswmdm/IMDSPStorage::GetAttributes","wmdm.imdspstorage_getattributes"]
old-location: wmdm\imdspstorage_getattributes.htm
tech.root: WMDM
ms.assetid: 822a5a3f-e649-4e5c-8216-56e77d60a8e3
ms.date: 12/05/2018
ms.keywords: GetAttributes, GetAttributes method [windows Media Device Manager], GetAttributes method [windows Media Device Manager],IMDSPStorage interface, IMDSPStorage interface [windows Media Device Manager],GetAttributes method, IMDSPStorage.GetAttributes, IMDSPStorage::GetAttributes, IMDSPStorageGetAttributes, mswmdm/IMDSPStorage::GetAttributes, wmdm.imdspstorage_getattributes
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
 - IMDSPStorage::GetAttributes
 - mswmdm/IMDSPStorage::GetAttributes
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
 - IMDSPStorage.GetAttributes
---

# IMDSPStorage::GetAttributes


## -description

The <b>GetAttributes</b> method retrieves the attributes of this storage object.

## -parameters

### -param pdwAttributes [out]

Pointer to a <b>DWORD</b> containing the attributes as defined by in the <b>IWMDMStorage::GetAttributes</b> method.

### -param pFormat [out]

Pointer to a <b>_WAVEFORMATEX</b> structure that is filled with attribute information about the object.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Evaluation of attributes is a crucial step when exposing the contents of the media device. Devices may not support hierarchical storage of data on storage media. The <b>GetAttributes</b> method allows the application to infer the support and format of the file system by discovering its structure through object attributes.

For example, the attributes of a top-level <b>IMDSPStorage</b> interface indicate a storage medium, and <b>IMDSPEnumStorage</b> exposes the contents of the medium. For an .mp3 file, the attributes indicate a file whose type can be determined by further examination of both the attributes and the file name. In a hierarchical medium, the attributes can indicate a directory whose contents can be exposed by <b>IMDSPStorage::EnumStorage</b>.

The <b>_WAVEFORMATEX</b> parameter is optional. If you pass a valid <b>_WAVEFORMATEX</b> pointer to an audio file, <b>GetAttributes</b> passes descriptive information back into the structure. However, if the file is not audio, the <b>_WAVEFORMATEX</b> parameter is ignored.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage">IMDSPEnumStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage2-getattributes2">IMDSPStorage2::GetAttributes2</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-setattributes">IMDSPStorage::SetAttributes</a>



<a href="/windows/desktop/WMDM/-waveformatex">_WAVEFORMATEX</a>