---
UID: NF:mswmdm.IMDSPStorage2.GetAttributes2
title: IMDSPStorage2::GetAttributes2 (mswmdm.h)
description: The GetAttributes2 method gets attributes of files or storages.
helpviewer_keywords: ["GetAttributes2","GetAttributes2 method [windows Media Device Manager]","GetAttributes2 method [windows Media Device Manager]","IMDSPStorage2 interface","IMDSPStorage2 interface [windows Media Device Manager]","GetAttributes2 method","IMDSPStorage2.GetAttributes2","IMDSPStorage2::GetAttributes2","IMDSPStorage2GetAttributes2","mswmdm/IMDSPStorage2::GetAttributes2","wmdm.imdspstorage2_getattributes2"]
old-location: wmdm\imdspstorage2_getattributes2.htm
tech.root: WMDM
ms.assetid: 2db30715-cd49-4e55-b0d0-73ac531f8661
ms.date: 12/05/2018
ms.keywords: GetAttributes2, GetAttributes2 method [windows Media Device Manager], GetAttributes2 method [windows Media Device Manager],IMDSPStorage2 interface, IMDSPStorage2 interface [windows Media Device Manager],GetAttributes2 method, IMDSPStorage2.GetAttributes2, IMDSPStorage2::GetAttributes2, IMDSPStorage2GetAttributes2, mswmdm/IMDSPStorage2::GetAttributes2, wmdm.imdspstorage2_getattributes2
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
 - IMDSPStorage2::GetAttributes2
 - mswmdm/IMDSPStorage2::GetAttributes2
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
 - IMDSPStorage2.GetAttributes2
---

# IMDSPStorage2::GetAttributes2


## -description

The <b>GetAttributes2</b> method gets attributes of files or storages.

## -parameters

### -param pdwAttributes [out]

Pointer to a <b>DWORD</b> containing the base attributes as defined in the <b>IWMDMStorage::GetAttributes</b> method.

### -param pdwAttributesEx [out]

Pointer to a <b>DWORD</b> containing the extended attributes. Currently no extended attributes are defined.

### -param pAudioFormat [out]

Pointer to a <b>_WAVEFORMATEX</b> structure that contains audio format information about the object. This parameter is optional and is ignored if the file is not audio.

### -param pVideoFormat [out]

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

See remarks for <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes">IWMDMStorage::GetAttributes</a>.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2">IMDSPStorage2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage2-setattributes2">IMDSPStorage2::SetAttributes2</a>