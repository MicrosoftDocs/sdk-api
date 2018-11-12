---
UID: NF:evr.IMFVideoPresenter.GetCurrentMediaType
title: IMFVideoPresenter::GetCurrentMediaType
author: windows-sdk-content
description: Retrieves the presenter's media type.
old-location: mf\imfvideopresenter_getcurrentmediatype.htm
tech.root: medfound
ms.assetid: 4b8f0e56-35de-4b4f-9897-32a7e14171c8
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 4b8f0e56-35de-4b4f-9897-32a7e14171c8, GetCurrentMediaType, GetCurrentMediaType method [Media Foundation], GetCurrentMediaType method [Media Foundation],IMFVideoPresenter interface, IMFVideoPresenter interface [Media Foundation],GetCurrentMediaType method, IMFVideoPresenter.GetCurrentMediaType, IMFVideoPresenter::GetCurrentMediaType, evr/IMFVideoPresenter::GetCurrentMediaType, mf.imfvideopresenter_getcurrentmediatype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoPresenter.GetCurrentMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoPresenter::GetCurrentMediaType


## -description



Retrieves the presenter's media type.




## -parameters




### -param ppMediaType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/9109b0dd-c44d-41d4-9480-1ca5c667dbd7">IMFVideoMediaType</a> interface. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The media type is not set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down

</td>
</tr>
</table>
 




## -remarks



This method returns the media type that the presenter sets for the mixer's output type. It describes the format of the composited image.




## -see-also




<a href="https://msdn.microsoft.com/1135b309-b158-4b70-9f76-5c93d0ad3250">How to Write an EVR Presenter</a>



<a href="https://msdn.microsoft.com/8f6e3132-03e9-4a2e-9160-e39d29cf2408">IMFVideoPresenter</a>
 

 

