---
UID: NN:tapi3.ITAMMediaFormat
title: ITAMMediaFormat
author: windows-driver-content
description: The ITAMMediaFormat interface sets and gets DirectShow media format.
old-location: tapi3\itammediaformat.htm
old-project: Tapi
ms.assetid: 82728afe-5743-4b45-86e6-32df021a2a5f
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITAMMediaFormat, ITAMMediaFormat interface [TAPI 2.2], ITAMMediaFormat interface [TAPI 2.2],described, _tapi3_itammediaformat, tapi3.itammediaformat, tapi3ds/ITAMMediaFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tapi3.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSP_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITAMMediaFormat
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAMMediaFormat interface


## -description


The 
<b>ITAMMediaFormat</b> interface sets and gets DirectShow media format. The format is described using the 
<b>AM_MEDIA_TYPE</b> structure. For more information on <b>AM_MEDIA_TYPE</b>, see the DirectX documentation. This interface is exposed on a 
<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a> only if an MSP is involved in terminal creation and implements this interface. The 
<b>ITAMMediaFormat</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>.

On addresses where a variety of formats are supported (such as Wave MSP addresses, which are used on most modems and voice boards), this media format must be set or the terminal will not be able to connect.

For other addresses, such as those implemented over IP, the format may be fixed/predetermined. In that case, a call to set format will fail if the format is not the same as the predetermined format.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAMMediaFormat</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITAMMediaFormat</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAMMediaFormat</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/384cd41e-b59a-4ac4-9687-cf0f0738dfe0">get_MediaFormat</a>
</td>
<td align="left" width="63%">
Gets the media format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/692df069-3016-46a2-9f33-4c709e85be1b">put_MediaFormat</a>
</td>
<td align="left" width="63%">
Sets the media format.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>
 

 

