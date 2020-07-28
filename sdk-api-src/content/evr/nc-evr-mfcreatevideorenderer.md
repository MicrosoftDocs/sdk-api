---
UID: NC:evr.MFCreateVideoRenderer
title: MFCreateVideoRenderer (evr.h)
description: Creates an instance of the enhanced video renderer (EVR) media sink.
helpviewer_keywords: ["MFCreateVideoRenderer","MFCreateVideoRenderer callback","MFCreateVideoRenderer callback function [Media Foundation]","d0f90c42-8f08-44f4-b3da-b9f3ae4869e6","evr/MFCreateVideoRenderer","mf.mfcreatevideorenderer"]
old-location: mf\mfcreatevideorenderer.htm
tech.root: mf
ms.assetid: d0f90c42-8f08-44f4-b3da-b9f3ae4869e6
ms.date: 12/05/2018
ms.keywords: MFCreateVideoRenderer, MFCreateVideoRenderer callback, MFCreateVideoRenderer callback function [Media Foundation], d0f90c42-8f08-44f4-b3da-b9f3ae4869e6, evr/MFCreateVideoRenderer, mf.mfcreatevideorenderer
f1_keywords:
- evr/MFCreateVideoRenderer
dev_langs:
- c++
req.header: evr.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- evr.h
api_name:
- MFCreateVideoRenderer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateVideoRenderer callback function


## -description



Creates an instance of the enhanced video renderer (EVR) media sink.




## -parameters




### -param riidRenderer [in]

Interface identifier (IID) of the requested interface on the EVR.


### -param ppVideoRenderer [out]

Receives a pointer to the requested interface. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -remarks



This function creates the Media Foundation version of the EVR. To create the DirectShow EVR filter, call <b>CoCreateInstance</b> with the class identifier CLSID_EnhancedVideoRenderer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

