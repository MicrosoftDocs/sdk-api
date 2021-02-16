---
UID: NF:mswmdm.IWMDMOperation2.GetObjectAttributes2
title: IWMDMOperation2::GetObjectAttributes2 (mswmdm.h)
description: Windows Media Device Manager calls GetObjectAttributes when a file is written to the device in order to learn the attributes of the file.
helpviewer_keywords: ["GetObjectAttributes2","GetObjectAttributes2 method [windows Media Device Manager]","GetObjectAttributes2 method [windows Media Device Manager]","IWMDMOperation2 interface","IWMDMOperation2 interface [windows Media Device Manager]","GetObjectAttributes2 method","IWMDMOperation2.GetObjectAttributes2","IWMDMOperation2::GetObjectAttributes2","IWMDMOperation2GetObjectAttributes2","mswmdm/IWMDMOperation2::GetObjectAttributes2","wmdm.iwmdmoperation2_getobjectattributes2"]
old-location: wmdm\iwmdmoperation2_getobjectattributes2.htm
tech.root: WMDM
ms.assetid: 7bf76094-5660-47ac-b1a2-a67b6f95964b
ms.date: 12/05/2018
ms.keywords: GetObjectAttributes2, GetObjectAttributes2 method [windows Media Device Manager], GetObjectAttributes2 method [windows Media Device Manager],IWMDMOperation2 interface, IWMDMOperation2 interface [windows Media Device Manager],GetObjectAttributes2 method, IWMDMOperation2.GetObjectAttributes2, IWMDMOperation2::GetObjectAttributes2, IWMDMOperation2GetObjectAttributes2, mswmdm/IWMDMOperation2::GetObjectAttributes2, wmdm.iwmdmoperation2_getobjectattributes2
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
 - IWMDMOperation2::GetObjectAttributes2
 - mswmdm/IWMDMOperation2::GetObjectAttributes2
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
 - IWMDMOperation2.GetObjectAttributes2
---

# IWMDMOperation2::GetObjectAttributes2


## -description

Windows Media Device Manager calls <b>GetObjectAttributes</b> when a file is written to the device in order to learn the attributes of the file.

## -parameters

### -param pdwAttributes [out]

Pointer to a <b>DWORD</b> specifying the storage attributes defined in the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes">IWMDMStorage::GetAttributes</a> method.

### -param pdwAttributesEx [out]

Pointer to a <b>DWORD</b> specifying extended attributes. There are currently no extended attributes defined.

### -param pAudioFormat [out]

Optional pointer to a <a href="/windows/desktop/WMDM/-waveformatex">_WAVEFORMATEX</a> structure that specifies audio file attributes.

### -param pVideoFormat [out]

Optional pointer to a <a href="/windows/desktop/WMDM/-videoinfoheader">_VIDEOINFOHEADER</a> structure that specifies video object attributes.

## -returns

The application should return one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The read operation should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The read operation should be cancelled without finishing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred, and the read operation should be cancelled without finishing.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2">IWMDMOperation2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation2-setobjectattributes2">SetObjectAttributes2</a>