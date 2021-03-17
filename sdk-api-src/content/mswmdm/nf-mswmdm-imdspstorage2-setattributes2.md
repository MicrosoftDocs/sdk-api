---
UID: NF:mswmdm.IMDSPStorage2.SetAttributes2
title: IMDSPStorage2::SetAttributes2 (mswmdm.h)
description: The SetAttributes2 method extends IMDSPStorage::SetAttributes by enabling you to set audio and video formats and extended attributes of a storage object.
helpviewer_keywords: ["IMDSPStorage2 interface [windows Media Device Manager]","SetAttributes2 method","IMDSPStorage2.SetAttributes2","IMDSPStorage2::SetAttributes2","IMDSPStorage2SetAttributes2","SetAttributes2","SetAttributes2 method [windows Media Device Manager]","SetAttributes2 method [windows Media Device Manager]","IMDSPStorage2 interface","mswmdm/IMDSPStorage2::SetAttributes2","wmdm.imdspstorage2_setattributes2"]
old-location: wmdm\imdspstorage2_setattributes2.htm
tech.root: WMDM
ms.assetid: f9c3f7e4-88b1-4842-aaaa-e6c52e1c3116
ms.date: 12/05/2018
ms.keywords: IMDSPStorage2 interface [windows Media Device Manager],SetAttributes2 method, IMDSPStorage2.SetAttributes2, IMDSPStorage2::SetAttributes2, IMDSPStorage2SetAttributes2, SetAttributes2, SetAttributes2 method [windows Media Device Manager], SetAttributes2 method [windows Media Device Manager],IMDSPStorage2 interface, mswmdm/IMDSPStorage2::SetAttributes2, wmdm.imdspstorage2_setattributes2
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
 - IMDSPStorage2::SetAttributes2
 - mswmdm/IMDSPStorage2::SetAttributes2
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
 - IMDSPStorage2.SetAttributes2
---

# IMDSPStorage2::SetAttributes2


## -description

The <b>SetAttributes2</b> method extends <b>IMDSPStorage::SetAttributes</b> by enabling you to set audio and video formats and extended attributes of a storage object.

## -parameters

### -param dwAttributes [in]

<b>DWORD</b> containing the attributes to be set as defined in the <b>IWMDMStorage::SetAttributes</b> method

### -param dwAttributesEx [in]

<b>DWORD</b> containing the extended attributes. No extended attributes are currently defined.

### -param pAudioFormat [in]

Pointer to a <b>_WAVEFORMATEX</b> structure that contains audio format information about the object. This parameter is optional and is ignored if the file is not audio.

### -param pVideoFormat [in]

Pointer to a <b>_VIDEOINFOHEADER</b> structure that contains video format information about the object. This parameter is optional and is ignored if the file is not video.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

See Remarks for <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes">IWMDMStorage::SetAttributes</a>.

This method is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2">IMDSPStorage2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage2-getattributes2">IMDSPStorage2::GetAttributes2</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-setattributes">IMDSPStorage::SetAttributes</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes">IWMDMStorage::SetAttributes</a>