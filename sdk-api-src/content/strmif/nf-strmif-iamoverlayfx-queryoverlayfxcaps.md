---
UID: NF:strmif.IAMOverlayFX.QueryOverlayFXCaps
title: IAMOverlayFX::QueryOverlayFXCaps (strmif.h)
author: windows-sdk-content
description: The QueryOverlayFXCaps method retrieves information about which overlay effects are available to the Overlay Mixer filter.
old-location: dshow\iamoverlayfx_queryoverlayfxcaps.htm
tech.root: DirectShow
ms.assetid: 01fdbe3d-bec7-4e66-87c5-b7e6c1044e8a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMOverlayFX interface [DirectShow],QueryOverlayFXCaps method, IAMOverlayFX.QueryOverlayFXCaps, IAMOverlayFX::QueryOverlayFXCaps, IAMOverlayFXQueryOverlayFXCaps, QueryOverlayFXCaps, QueryOverlayFXCaps method [DirectShow], QueryOverlayFXCaps method [DirectShow],IAMOverlayFX interface, dshow.iamoverlayfx_queryoverlayfxcaps, strmif/IAMOverlayFX::QueryOverlayFXCaps
ms.topic: method
f1_keywords: ["strmif/IAMOverlayFX.QueryOverlayFXCaps"]
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMOverlayFX.QueryOverlayFXCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMOverlayFX::QueryOverlayFXCaps


## -description



The <code>QueryOverlayFXCaps</code> method retrieves information about which overlay effects are available to the Overlay Mixer filter.




## -parameters




### -param lpdwOverlayFXCaps [out]

Pointer to a variable that receives a value indicating the overlay effects capabilities of the overlay surface. The value is a logical combination of flags from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-amoverlayfx">AMOVERLAYFX</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamoverlayfx">IAMOverlayFX Interface</a>
 

 

