---
UID: NF:strmif.IFilterMapper2.RegisterFilter
title: IFilterMapper2::RegisterFilter (strmif.h)
description: The RegisterFilter method adds filter information to the registry.
helpviewer_keywords: ["IFilterMapper2 interface [DirectShow]","RegisterFilter method","IFilterMapper2.RegisterFilter","IFilterMapper2::RegisterFilter","IFilterMapper2RegisterFilter","RegisterFilter","RegisterFilter method [DirectShow]","RegisterFilter method [DirectShow]","IFilterMapper2 interface","dshow.ifiltermapper2_registerfilter","strmif/IFilterMapper2::RegisterFilter"]
old-location: dshow\ifiltermapper2_registerfilter.htm
tech.root: dshow
ms.assetid: 773e527e-2174-4f74-a822-549cfe2927a3
ms.date: 4/26/2023
ms.keywords: IFilterMapper2 interface [DirectShow],RegisterFilter method, IFilterMapper2.RegisterFilter, IFilterMapper2::RegisterFilter, IFilterMapper2RegisterFilter, RegisterFilter, RegisterFilter method [DirectShow], RegisterFilter method [DirectShow],IFilterMapper2 interface, dshow.ifiltermapper2_registerfilter, strmif/IFilterMapper2::RegisterFilter
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterMapper2::RegisterFilter
 - strmif/IFilterMapper2::RegisterFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterMapper2.RegisterFilter
---

# IFilterMapper2::RegisterFilter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>RegisterFilter</code> method adds filter information to the registry.

## -parameters

### -param clsidFilter [in]

Class identifier (CLSID) of the filter.

### -param Name [in]

Descriptive name for the filter.

### -param ppMoniker [in, out]

Address of a pointer to a device moniker that determines where this filter's data will be written. Can be <b>NULL</b>.

### -param pclsidCategory [in]

Pointer to the filter category of the filter. If <b>NULL</b>, the default category is CLSID_ActiveMovieFilters. (See <a href="/windows/desktop/DirectShow/filter-categories">Filter Categories</a>.)

### -param szInstance [in]

Instance data for constructing the device moniker's display name. Can be the friendly name, or the string representation of the filter CLSID. If <b>NULL</b>, defaults to the filter CLSID.

### -param prf2 [in]

Pointer to a <a href="/windows/desktop/api/strmif/ns-strmif-regfilter2">REGFILTER2</a> structure containing filter information.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_BAD_KEY</b></dt>
</dl>
</td>
<td width="60%">
Could not get registry key.

</td>
</tr>
</table>

## -remarks

This method adds information about the filter to the registry, under the registry entry for the specified filter category. It does not register the in-process server that creates the filter (usually a DLL). To register the server, you can call the <a href="/windows/desktop/DirectShow/amoviedllregisterserver2">AMovieDllRegisterServer2</a> function.

For the <i>ppMoniker</i> parameter, use one of the following:

<ul>
<li>The address of an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface pointer for an existing device moniker</li>
<li>The address of a <b>NULL</b><b>IMoniker</b> interface pointer</li>
<li><b>NULL</b></li>
</ul>
If you are registering a filter for a Windows Driver Model (WDM) or Plug and Play device, pass the address of the existing device moniker. The filter will be registered using this moniker. When the method returns, <i>*ppMoniker</i> is set to <b>NULL</b>.

Otherwise, the method creates a new moniker. If <i>ppMoniker</i> is non-<b>NULL</b>, the method sets <i>*ppMoniker</i> to point to the new moniker. The application can use this moniker to write additional private values in the property bag. Be sure to release the interface.

Set <i>ppMoniker</i> to <b>NULL</b> if you don't want to provide or receive the moniker.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2 Interface</a>