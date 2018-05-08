---
UID: NF:strmif.IMediaSeeking.GetCapabilities
title: IMediaSeeking::GetCapabilities
author: windows-driver-content
description: The GetCapabilities method retrieves all the seeking capabilities of the stream.
old-location: dshow\imediaseeking_getcapabilities.htm
old-project: DirectShow
ms.assetid: 84dd3c21-9c72-4433-bd03-29520dc138ca
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: GetCapabilities, GetCapabilities method [DirectShow], GetCapabilities method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetCapabilities method, IMediaSeeking.GetCapabilities, IMediaSeeking::GetCapabilities, IMediaSeekingGetCapabilities, dshow.imediaseeking_getcapabilities, strmif/IMediaSeeking::GetCapabilities
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaSeeking.GetCapabilities
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaSeeking::GetCapabilities


## -description



The <code>GetCapabilities</code> method retrieves all the seeking capabilities of the stream.




## -parameters




### -param pCapabilities [out]

Pointer to a variable that receives a bitwise combination of <a href="https://msdn.microsoft.com/1c7ad11b-2d10-409e-a292-b777566c637d">AM_SEEKING_SEEKING_CAPABILITIES</a> flags.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



This method returns information on all the seeking capabilities of the stream. Examine <i>pCapabilities</i> by performing a separate bitwise-AND operation on each AM_SEEKING_SEEKING_CAPABILITIES value you are interested in.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
DWORD dwCaps = 0;
pMediaSeeking-&gt;GetCapabilities(&amp;dwCaps);

if (dwCaps &amp; AM_SEEKING_CanGetCurrentPos) 
{
    // The stream can seek to the current position.
}
if (dwCaps &amp; AM_SEEKING_CanPlayBackwards) 
{
    // The stream can play backward.
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking Interface</a>
 

 

