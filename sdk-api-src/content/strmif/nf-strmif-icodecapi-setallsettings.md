---
UID: NF:strmif.ICodecAPI.SetAllSettings
title: ICodecAPI::SetAllSettings (strmif.h)
author: windows-sdk-content
description: The SetAllSettings method reads codec properties from a stream and sets them on the codec.
old-location: dshow\icodecapi_setallsettings.htm
tech.root: DirectShow
ms.assetid: 1148e380-a4fc-4392-861e-8ea695060032
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICodecAPI interface [DirectShow],SetAllSettings method, ICodecAPI.SetAllSettings, ICodecAPI::SetAllSettings, ICodecAPISetAllSettings, SetAllSettings, SetAllSettings method [DirectShow], SetAllSettings method [DirectShow],ICodecAPI interface, dshow.icodecapi_setallsettings, strmif/ICodecAPI::SetAllSettings
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
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
 - ICodecAPI.SetAllSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICodecAPI::SetAllSettings


## -description


The <b>SetAllSettings</b> method reads codec properties from a stream and sets them on the codec.


## -parameters




### -param __MIDL__ICodecAPI0001 [in]

Pointer to the <b>IStream</b> interface of the stream.
          


## -returns



This method can return one of these values.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>
 




## -remarks



Codecs that implement <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a> are  not required to support this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-getvalue">ICodecAPI::GetValue</a>
 

 

