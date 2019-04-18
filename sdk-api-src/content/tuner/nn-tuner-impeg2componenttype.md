---
UID: NN:tuner.IMPEG2ComponentType
title: IMPEG2ComponentType (tuner.h)
author: windows-sdk-content
description: The IMPEG2ComponentType interface is implemented on MPEG2ComponentType objects. It enables applications to set and retrieve information about MPEG2 stream types.
old-location: mstv\impeg2componenttype.htm
tech.root: mstv
ms.assetid: 10bf35e0-d5bf-41ed-b514-7c1bfaf774a0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMPEG2ComponentType, IMPEG2ComponentType interface [Microsoft TV Technologies], IMPEG2ComponentType interface [Microsoft TV Technologies],described, IMPEG2ComponentTypeInterface, mstv.impeg2componenttype, tuner/IMPEG2ComponentType
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IMPEG2ComponentType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMPEG2ComponentType interface


## -description



The <b>IMPEG2ComponentType</b> interface is implemented on <a href="https://msdn.microsoft.com/16059b17-9145-4aad-97ce-c31fdfe1db69">MPEG2ComponentType</a> objects. It enables applications to set and retrieve information about MPEG2 stream types.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2ComponentType</b> interface inherits from <a href="https://msdn.microsoft.com/775b5e8d-d9ed-4371-a651-bfeed6fa0ad5">ILanguageComponentType</a>. <b>IMPEG2ComponentType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2ComponentType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3aa2a63-aa02-41c3-bbdf-f155346eea0a">get_StreamType</a>
</td>
<td align="left" width="63%">
Retrieves the stream type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dbfacf3-87e2-48d4-add9-6da68c56af82">put_StreamType</a>
</td>
<td align="left" width="63%">
Sets the stream type.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2ComponentType)</code>.




## -see-also




<a href="https://msdn.microsoft.com/775b5e8d-d9ed-4371-a651-bfeed6fa0ad5">ILanguageComponentType</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

