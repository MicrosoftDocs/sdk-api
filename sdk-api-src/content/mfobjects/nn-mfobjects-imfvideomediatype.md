---
UID: NN:mfobjects.IMFVideoMediaType
title: IMFVideoMediaType
author: windows-sdk-content
description: Represents a description of a video format.
old-location: mf\imfvideomediatype.htm
old-project: medfound
ms.assetid: 9109b0dd-c44d-41d4-9480-1ca5c667dbd7
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: 9109b0dd-c44d-41d4-9480-1ca5c667dbd7, IMFVideoMediaType, IMFVideoMediaType interface [Media Foundation], IMFVideoMediaType interface [Media Foundation],described, mf.imfvideomediatype, mfobjects/IMFVideoMediaType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfobjects.h
req.include-header: Mfidl.h
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
req.typenames: MF_FILE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFVideoMediaType
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFVideoMediaType interface


## -description


Represents a description of a video format.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoMediaType</b> interface inherits from <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>. <b>IMFVideoMediaType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoMediaType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2168c76e-2b83-40ad-8ac1-9b76f1a31b7b">GetVideoFormat</a>
</td>
<td align="left" width="63%">
Returns a pointer to an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure that describes the video format. (Deprecated.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f8fddef-b9b8-4473-a8d0-d6e44ad32648">GetVideoRepresentation</a>
</td>
<td align="left" width="63%">
Retrieves an alternative representation of the media type. (Deprecated.)

</td>
</tr>
</table> 


## -remarks



If the major type of a media type is MFMediaType_Video, you can query the media type object for the <b>IMFVideoMediaType</b> interface.

Applications should avoid using this interface except when a method or function requires an <b>IMFVideoMediaType</b> pointer as a parameter. You can get all of the format information from a video media type through the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface, which <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> inherits.




## -see-also




<a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/e84ba3f6-4857-4340-baca-5847650ea7b8">Media Type Attributes</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

