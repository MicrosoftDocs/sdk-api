---
UID: NF:strmif.IMediaSeeking.GetPreroll
title: IMediaSeeking::GetPreroll
author: windows-sdk-content
description: The GetPreroll method retrieves the amount of data that will be queued before the start position.
old-location: dshow\imediaseeking_getpreroll.htm
tech.root: DirectShow
ms.assetid: 9d519aab-eb35-4a00-b6fe-23d734f969ae
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPreroll, GetPreroll method [DirectShow], GetPreroll method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetPreroll method, IMediaSeeking.GetPreroll, IMediaSeeking::GetPreroll, IMediaSeekingGetPreroll, dshow.imediaseeking_getpreroll, strmif/IMediaSeeking::GetPreroll
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaSeeking.GetPreroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSeeking::GetPreroll


## -description



The <code>GetPreroll</code> method retrieves the amount of data that will be queued before the start position.




## -parameters




### -param pllPreroll [out]

Pointer to a variable that receives the preroll time, in units of the current time format.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

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
</table>
 




## -remarks



The <i>preroll</i> is the time prior to the start position at which nonrandom access devices, such as tape players, should start rolling.

The returned value is expressed in the current time format. The default time format is <a href="https://msdn.microsoft.com/862c95bc-2e0a-42c0-b907-45f64f27bd41">REFERENCE_TIME</a> units (100 nanoseconds). To change time formats, use the <a href="https://msdn.microsoft.com/b6f64f8a-67b8-4297-8f0d-389001fa1681">IMediaSeeking::SetTimeFormat</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking Interface</a>
 

 

