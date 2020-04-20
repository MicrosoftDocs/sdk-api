---
UID: NN:wmsbuffer.INSSBuffer4
title: INSSBuffer4 (wmsbuffer.h)
description: The INSSBuffer4 interface provides methods to enumerate buffer properties.helpviewer_keywords: ["INSSBuffer4","INSSBuffer4 interface [windows Media Format]","INSSBuffer4 interface [windows Media Format]","described","INSSBuffer4Interface","wmformat.inssbuffer4","wmsbuffer/INSSBuffer4"]
old-location: wmformat\inssbuffer4.htm
tech.root: wmformat
ms.assetid: d6531e52-b58b-46ed-a47b-444cd98e1ec5
ms.date: 12/05/2018
ms.keywords: INSSBuffer4, INSSBuffer4 interface [windows Media Format], INSSBuffer4 interface [windows Media Format],described, INSSBuffer4Interface, wmformat.inssbuffer4, wmsbuffer/INSSBuffer4
f1_keywords:
- wmsbuffer/INSSBuffer4
dev_langs:
- c++
req.header: wmsbuffer.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsbuffer.h
api_name:
- INSSBuffer4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INSSBuffer4 interface


## -description



The <b>INSSBuffer4</b> interface provides methods to enumerate buffer properties. These methods are important when reading files that may have properties of which you are not aware.

An <b>INSSBuffer4</b> interface exists for every buffer object. To retrieve a pointer to an instance of <b>INSSBuffer4</b>, call the <b>QueryInterface</b> method of one of the other interfaces in the buffer object, typically <a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a>.



The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a>
</td>
<td>IID_INSSBuffer</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2">INSSBuffer2</a>
</td>
<td>IID_INSSBuffer2</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3</a>
</td>
<td>IID_INSSBuffer3</td>
</tr>
</table>
 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INSSBuffer4</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3</a>. <b>INSSBuffer4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INSSBuffer4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer4-getpropertybyindex">GetPropertyByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a buffer property, also called a data unit extension, using an index instead of a name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer4-getpropertycount">GetPropertyCount</a>
</td>
<td align="left" width="63%">
Retrieves the total count of buffer properties associated with the sample.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

