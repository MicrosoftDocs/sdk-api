---
UID: NF:mswmdm.IWMDMStorage2.GetAttributes2
title: IWMDMStorage2::GetAttributes2 (mswmdm.h)
description: The GetAttributes2 method retrieves extended attributes of the storage.
helpviewer_keywords: ["GetAttributes2","GetAttributes2 method [windows Media Device Manager]","GetAttributes2 method [windows Media Device Manager]","IWMDMStorage2 interface","IWMDMStorage2 interface [windows Media Device Manager]","GetAttributes2 method","IWMDMStorage2.GetAttributes2","IWMDMStorage2::GetAttributes2","IWMDMStorage2GetAttributes2","mswmdm/IWMDMStorage2::GetAttributes2","wmdm.iwmdmstorage2_getattributes2"]
old-location: wmdm\iwmdmstorage2_getattributes2.htm
tech.root: WMDM
ms.assetid: 8212ab78-0a2a-41cd-8a7c-da6e3886b586
ms.date: 12/05/2018
ms.keywords: GetAttributes2, GetAttributes2 method [windows Media Device Manager], GetAttributes2 method [windows Media Device Manager],IWMDMStorage2 interface, IWMDMStorage2 interface [windows Media Device Manager],GetAttributes2 method, IWMDMStorage2.GetAttributes2, IWMDMStorage2::GetAttributes2, IWMDMStorage2GetAttributes2, mswmdm/IWMDMStorage2::GetAttributes2, wmdm.iwmdmstorage2_getattributes2
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
 - IWMDMStorage2::GetAttributes2
 - mswmdm/IWMDMStorage2::GetAttributes2
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
 - IWMDMStorage2.GetAttributes2
---

# IWMDMStorage2::GetAttributes2


## -description

The <b>GetAttributes2</b> method retrieves extended attributes of the storage.

## -parameters

### -param pdwAttributes [out]

Pointer to a <b>DWORD</b> specifying one or more attributes defined in the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes">IWMDMStorage::GetAttributes</a> method, combined with a bitwise <b>OR</b>.

### -param pdwAttributesEx [out]

Pointer to a <b>DWORD</b> specifying the extended attributes. Currently, no extended attributes are defined.

### -param pAudioFormat [out]

Optional pointer to a <a href="/windows/desktop/WMDM/-waveformatex">_ WAVEFORMATEX</a> structure that specifies audio information about the object. This parameter is ignored if the file is not audio.

### -param pVideoFormat [out]

Optional pointer to a <a href="/windows/desktop/WMDM/-videoinfoheader">_ VIDEOINFOHEADER</a> structure that specifies video information about the object. This parameter is ignored if the file is not video.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Evaluation of attributes is a crucial step when exposing the contents of the media device. Some devices do not support hierarchical storage of data on storage media. The <b>GetAttributes2</b> method is used to infer the support and format of the file system by discovering its structure through object attributes.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2">IWMDMStorage2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2">IWMDMStorage2::SetAttributes2</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage">IWMDMStorage::EnumStorage</a>