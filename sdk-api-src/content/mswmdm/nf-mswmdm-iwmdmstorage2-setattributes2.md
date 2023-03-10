---
UID: NF:mswmdm.IWMDMStorage2.SetAttributes2
title: IWMDMStorage2::SetAttributes2 (mswmdm.h)
description: The SetAttributes2 method sets extended attributes of the storage.
helpviewer_keywords: ["IWMDMStorage2 interface [windows Media Device Manager]","SetAttributes2 method","IWMDMStorage2.SetAttributes2","IWMDMStorage2::SetAttributes2","IWMDMStorage2SetAttributes2","SetAttributes2","SetAttributes2 method [windows Media Device Manager]","SetAttributes2 method [windows Media Device Manager]","IWMDMStorage2 interface","mswmdm/IWMDMStorage2::SetAttributes2","wmdm.iwmdmstorage2_setattributes2"]
old-location: wmdm\iwmdmstorage2_setattributes2.htm
tech.root: WMDM
ms.assetid: 0a2e143e-8d6a-497e-9c45-fd3349c4ec97
ms.date: 12/05/2018
ms.keywords: IWMDMStorage2 interface [windows Media Device Manager],SetAttributes2 method, IWMDMStorage2.SetAttributes2, IWMDMStorage2::SetAttributes2, IWMDMStorage2SetAttributes2, SetAttributes2, SetAttributes2 method [windows Media Device Manager], SetAttributes2 method [windows Media Device Manager],IWMDMStorage2 interface, mswmdm/IWMDMStorage2::SetAttributes2, wmdm.iwmdmstorage2_setattributes2
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
 - IWMDMStorage2::SetAttributes2
 - mswmdm/IWMDMStorage2::SetAttributes2
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
 - IWMDMStorage2.SetAttributes2
---

# IWMDMStorage2::SetAttributes2


## -description

The <b>SetAttributes2</b> method sets extended attributes of the storage.

## -parameters

### -param dwAttributes [in]

<b>DWORD</b> specifying the base attributes defined in the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes">IWMDMStorage::SetAttributes</a> method.

### -param dwAttributesEx [in]

<b>DWORD</b> specifying extended attributes. Currently, no extended attributes are defined.

### -param pFormat [out]

Optional pointer to a <a href="/windows/desktop/WMDM/-waveformatex">_ WAVEFORMATEX</a> structure that specifies audio information about the object. This parameter is ignored if the file is not audio.

### -param pVideoFormat [in]

Optional pointer to a <a href="/windows/desktop/WMDM/-videoinfoheader">_VIDEOINFOHEADER</a> structure that specifies video information about the object. This parameter is ignored if the file is not video.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2">IWMDMStorage2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2">IWMDMStorage2::GetAttributes2</a>