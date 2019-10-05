---
UID: NF:vidcap.IVideoProcAmp.put_ColorEnable
title: IVideoProcAmp::put_ColorEnable (vidcap.h)
author: windows-sdk-content
description: The put_ColorEnable method sets the camera's color-enable setting.
old-location: dshow\ivideoprocamp_put_colorenable.htm
tech.root: DirectShow
ms.assetid: 6a1caa3f-e591-4176-90b9-80a4bd71533b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_ColorEnable method, IVideoProcAmp.put_ColorEnable, IVideoProcAmp::put_ColorEnable, IVideoProcAmpput_ColorEnable, dshow.ivideoprocamp_put_colorenable, put_ColorEnable, put_ColorEnable method [DirectShow], put_ColorEnable method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_ColorEnable
ms.topic: method
f1_keywords: 
 - "vidcap/IVideoProcAmp.put_ColorEnable"
dev_langs:
 - c++
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IVideoProcAmp.put_ColorEnable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoProcAmp::put_ColorEnable


## -description


The <code>put_ColorEnable</code> method sets the camera's color-enable setting.


## -parameters




### -param Value [in]

Specifies one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Color disabled.</td>
</tr>
<tr>
<td>1</td>
<td>Color enabled.</td>
</tr>
</table>
 


### -param Flags [in]

Zero or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
 

 

