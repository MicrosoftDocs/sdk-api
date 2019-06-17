---
UID: NF:textstor.IAnchor.SetGravity
title: IAnchor::SetGravity (textstor.h)
author: windows-sdk-content
description: IAnchor::SetGravity method
old-location: tsf\ianchor_setgravity.htm
tech.root: TSF
ms.assetid: c532abcf-9ae0-4566-80f7-0bb4ae908fce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAnchor interface [Text Services Framework],SetGravity method, IAnchor.SetGravity, IAnchor::SetGravity, SetGravity, SetGravity method [Text Services Framework], SetGravity method [Text Services Framework],IAnchor interface, textstor/IAnchor::SetGravity, tsf.ianchor_setgravity
ms.topic: method
f1_keywords: ["textstor/IAnchor.SetGravity"]
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - IAnchor.SetGravity
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IAnchor::SetGravity


## -description




## -parameters




### -param gravity [in]

Contains a value from the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/ne-textstor-__midl_ianchor_0001">TsGravity</a> enumeration that specifies a new forward or backward gravity for the anchor.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/ranges">Anchor Gravity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-ianchor">IAnchor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-ianchor-getgravity">IAnchor::GetGravity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/ne-textstor-__midl_ianchor_0001">TsGravity</a>
 

 

