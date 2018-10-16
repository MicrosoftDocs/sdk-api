---
UID: NN:mfobjects.IMFMediaType
title: IMFMediaType
author: windows-sdk-content
description: Represents a description of a media format.
old-location: mf\imfmediatype.htm
tech.root: medfound
ms.assetid: f1d60bec-71e4-4fcc-a020-92754b6f3c02
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFMediaType, IMFMediaType interface [Media Foundation], IMFMediaType interface [Media Foundation],described, f1d60bec-71e4-4fcc-a020-92754b6f3c02, mf.imfmediatype, mfobjects/IMFMediaType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaType interface


## -description


Represents a description of a media format.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaType</b> interface inherits from <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>. <b>IMFMediaType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2007f16-543f-4f05-a44d-b4b4ae8019fb">FreeRepresentation</a>
</td>
<td align="left" width="63%">
Frees memory that was allocated by the <a href="https://msdn.microsoft.com/2135ff86-a3b6-4e1c-a9de-867f4828f008">GetRepresentation</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98f0a9ca-4766-4d2b-89b8-d6e30b75f47d">GetMajorType</a>
</td>
<td align="left" width="63%">
Retrieves the major type of the format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2135ff86-a3b6-4e1c-a9de-867f4828f008">GetRepresentation</a>
</td>
<td align="left" width="63%">
Retrieves an alternative representation of the media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d15d683b-f2ce-40ac-9724-a0785f5d335c">IsCompressedFormat</a>
</td>
<td align="left" width="63%">
Queries whether the media type is a compressed format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42b5b0e8-3b13-4bda-a53c-0428a3c9b131">IsEqual</a>
</td>
<td align="left" width="63%">
Compares two media types and determines whether they are identical.

</td>
</tr>
</table> 


## -remarks



To create a new media type, call <a href="https://msdn.microsoft.com/05b0941e-03ce-4ced-9022-22b65d1c4b4c">MFCreateMediaType</a>.
      

All of the information in a media type is stored as attributes. To clone a media type, call <a href="https://msdn.microsoft.com/111b55bc-fb8e-45b5-a709-703acd23c4be">IMFAttributes::CopyAllItems</a>.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/e84ba3f6-4857-4340-baca-5847650ea7b8">Media Type Attributes</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

