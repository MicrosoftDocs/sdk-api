---
UID: NF:dxva2api.IDirectXVideoMemoryConfiguration.GetAvailableSurfaceTypeByIndex
title: IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex (dxva2api.h)
description: Retrieves a supported video surface type.
helpviewer_keywords: ["63311052-f01b-4d77-afac-1cc89166f754","GetAvailableSurfaceTypeByIndex","GetAvailableSurfaceTypeByIndex method [Media Foundation]","GetAvailableSurfaceTypeByIndex method [Media Foundation]","IDirectXVideoMemoryConfiguration interface","IDirectXVideoMemoryConfiguration interface [Media Foundation]","GetAvailableSurfaceTypeByIndex method","IDirectXVideoMemoryConfiguration.GetAvailableSurfaceTypeByIndex","IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex","dxva2api/IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex","mf.idirectxvideomemoryconfiguration_getavailablesurfacetypebyindex"]
old-location: mf\idirectxvideomemoryconfiguration_getavailablesurfacetypebyindex.htm
tech.root: medfound
ms.assetid: 63311052-f01b-4d77-afac-1cc89166f754
ms.date: 12/05/2018
ms.keywords: 63311052-f01b-4d77-afac-1cc89166f754, GetAvailableSurfaceTypeByIndex, GetAvailableSurfaceTypeByIndex method [Media Foundation], GetAvailableSurfaceTypeByIndex method [Media Foundation],IDirectXVideoMemoryConfiguration interface, IDirectXVideoMemoryConfiguration interface [Media Foundation],GetAvailableSurfaceTypeByIndex method, IDirectXVideoMemoryConfiguration.GetAvailableSurfaceTypeByIndex, IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex, dxva2api/IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex, mf.idirectxvideomemoryconfiguration_getavailablesurfacetypebyindex
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex
 - dxva2api/IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoMemoryConfiguration.GetAvailableSurfaceTypeByIndex
---

# IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex


## -description

Retrieves a supported video surface type.

## -parameters

### -param dwTypeIndex [in]

Zero-based index of the surface type to retrieve. Surface types are indexed in order of preference, starting with the most preferred type.

### -param pdwType [out]

Receives a member of the <a href="/windows/win32/api/dxva2api/ne-dxva2api-dxva2_surfacetype">DXVA2_SurfaceType</a> enumeration that specifies the surface type.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_MORE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
The index was out of range.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration">IDirectXVideoMemoryConfiguration</a>



<a href="/windows/desktop/medfound/supporting-dxva-2-0-in-directshow">Supporting DXVA 2.0 in DirectShow</a>