---
UID: NC:evr.MFCreateVideoRenderer
title: MFCreateVideoRenderer
author: windows-sdk-content
description: Creates an instance of the enhanced video renderer (EVR) media sink.
old-location: mf\mfcreatevideorenderer.htm
old-project: medfound
ms.assetid: d0f90c42-8f08-44f4-b3da-b9f3ae4869e6
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFCreateVideoRenderer, MFCreateVideoRenderer callback, MFCreateVideoRenderer callback function [Media Foundation], d0f90c42-8f08-44f4-b3da-b9f3ae4869e6, evr/MFCreateVideoRenderer, mf.mfcreatevideorenderer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: evr.h
req.include-header: 
req.redist: 
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
req.typenames: TRACE_PROVIDER_INSTANCE_INFO, *PTRACE_PROVIDER_INSTANCE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - evr.h
api_name:
 - MFCreateVideoRenderer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

