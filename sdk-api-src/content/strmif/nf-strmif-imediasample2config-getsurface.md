---
UID: NF:strmif.IMediaSample2Config.GetSurface
title: IMediaSample2Config::GetSurface
author: windows-sdk-content
description: The GetSurface method returns a pointer to the Direct3D surface managed by this media sample.
old-location: dshow\imediasample2config_getsurface.htm
old-project: DirectShow
ms.assetid: c53306ec-cb5c-4f55-afb0-de72386a166d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetSurface, GetSurface method [DirectShow], GetSurface method [DirectShow],IMediaSample2Config interface, IMediaSample2Config interface [DirectShow],GetSurface method, IMediaSample2Config.GetSurface, IMediaSample2Config::GetSurface, IMediaSample2ConfigGetSurface, dshow.imediasample2config_getsurface, strmif/IMediaSample2Config::GetSurface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaSample2Config.GetSurface
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaSample2Config::GetSurface


## -description



The <code>GetSurface</code> method returns a pointer to the Direct3D surface managed by this media sample.




## -parameters




### -param ppDirect3DSurface9 [out]

Receives a pointer to the <b>IUnknown</b> interface of the Direct3D surface. The caller must release the interface.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/99a3d957-b504-4242-87de-54b5468f00b5">IMediaSample2Config Interface</a>
 

 

