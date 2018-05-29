---
UID: NF:amvideo.IFullScreenVideoEx.CountModes
title: IFullScreenVideoEx::CountModes
author: windows-sdk-content
description: The CountModes method retrieves the number of display modes that the Full Screen Renderer supports.
old-location: dshow\ifullscreenvideoex_countmodes.htm
old-project: DirectShow
ms.assetid: 70d4e124-083b-4729-8f39-778e815ea23b
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: CountModes, CountModes method [DirectShow], CountModes method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoCountModes, IFullScreenVideoEx interface [DirectShow],CountModes method, IFullScreenVideoEx.CountModes, IFullScreenVideoEx::CountModes, amvideo/IFullScreenVideoEx::CountModes, dshow.ifullscreenvideoex_countmodes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amvideo.h
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
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IFullScreenVideoEx.CountModes
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IFullScreenVideoEx::CountModes


## -description



The <code>CountModes</code> method retrieves the number of display modes that the Full Screen Renderer supports.




## -parameters




### -param pModes [out]

Pointer to the returned mode count.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

