---
UID: NF:mswmdm.IWMDMOperation2.SetObjectAttributes2
title: IWMDMOperation2::SetObjectAttributes2 (mswmdm.h)
description: The SetObjectAttributes2 method sets attributes of files or storages. This method is currently not called by Windows Media Device Manager.
helpviewer_keywords: ["IWMDMOperation2 interface [windows Media Device Manager]","SetObjectAttributes2 method","IWMDMOperation2.SetObjectAttributes2","IWMDMOperation2::SetObjectAttributes2","IWMDMOperation2SetObjectAttributes2","SetObjectAttributes2","SetObjectAttributes2 method [windows Media Device Manager]","SetObjectAttributes2 method [windows Media Device Manager]","IWMDMOperation2 interface","mswmdm/IWMDMOperation2::SetObjectAttributes2","wmdm.iwmdmoperation2_setobjectattributes2"]
old-location: wmdm\iwmdmoperation2_setobjectattributes2.htm
tech.root: WMDM
ms.assetid: ce19bfe5-c8ff-40f4-a152-8a46d2576c63
ms.date: 12/05/2018
ms.keywords: IWMDMOperation2 interface [windows Media Device Manager],SetObjectAttributes2 method, IWMDMOperation2.SetObjectAttributes2, IWMDMOperation2::SetObjectAttributes2, IWMDMOperation2SetObjectAttributes2, SetObjectAttributes2, SetObjectAttributes2 method [windows Media Device Manager], SetObjectAttributes2 method [windows Media Device Manager],IWMDMOperation2 interface, mswmdm/IWMDMOperation2::SetObjectAttributes2, wmdm.iwmdmoperation2_setobjectattributes2
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
 - IWMDMOperation2::SetObjectAttributes2
 - mswmdm/IWMDMOperation2::SetObjectAttributes2
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
 - IWMDMOperation2.SetObjectAttributes2
---

# IWMDMOperation2::SetObjectAttributes2


## -description

The <b>SetObjectAttributes2</b> method sets attributes of files or storages. This method is currently not called by Windows Media Device Manager.

## -parameters

### -param dwAttributes [in]

Pointer to a <b>DWORD</b> specifying the attributes as defined by the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes">IWMDMStorage::SetAttributes</a> method.

### -param dwAttributesEx [in]

<b>DWORD</b> specifying the extended attributes. No extended attributes are currently defined.

### -param pFormat [in]

Optional pointer to a <a href="/windows/desktop/WMDM/-waveformatex">_WAVEFORMATEX</a> structure that specifies audio information about the object.

### -param pVideoFormat [in]

Optional pointer to a <a href="/windows/desktop/WMDM/-videoinfoheader">_VIDEOINFOHEADER</a> structure that specifies video information about the object.

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

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation2-getobjectattributes2">GetObjectAttributes2</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2">IWMDMOperation2 Interface</a>