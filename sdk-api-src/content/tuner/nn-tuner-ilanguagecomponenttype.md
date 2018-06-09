---
UID: NN:tuner.ILanguageComponentType
title: ILanguageComponentType
author: windows-sdk-content
description: The ILanguageComponentType interface is implemented on LanguageComponentType objects. It provides methods that define the language of the stream content. Not all streams have a language component.
old-location: mstv\ilanguagecomponenttype.htm
old-project: mstv
ms.assetid: 775b5e8d-d9ed-4371-a651-bfeed6fa0ad5
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ILanguageComponentType, ILanguageComponentType interface [Microsoft TV Technologies], ILanguageComponentType interface [Microsoft TV Technologies],described, ILanguageComponentTypeInterface, mstv.ilanguagecomponenttype, tuner/ILanguageComponentType
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ILanguageComponentType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ILanguageComponentType interface


## -description



The <b>ILanguageComponentType</b> interface is implemented on <a href="https://msdn.microsoft.com/d1601651-84a2-4fd8-9318-653aa569e747">LanguageComponentType</a> objects. It provides methods that define the language of the stream content. Not all streams have a language component.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILanguageComponentType</b> interface inherits from <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a>. <b>ILanguageComponentType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILanguageComponentType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f70dcc70-701a-4465-ad40-1ddc5e697f46">get_LangID</a>
</td>
<td align="left" width="63%">
Retrieves the language of the stream content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0dc0141-a839-4fdc-9313-24ddd3eaf63d">put_LangID</a>
</td>
<td align="left" width="63%">
Sets the language of the stream content.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ILanguageComponentType)</code>.




## -see-also




<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

