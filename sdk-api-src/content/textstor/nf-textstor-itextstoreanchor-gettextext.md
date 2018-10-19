---
UID: NF:textstor.ITextStoreAnchor.GetTextExt
title: ITextStoreAnchor::GetTextExt
author: windows-sdk-content
description: The ITextStoreAnchor::GetTextExt method returns the bounding box, in screen coordinates, of a range of text. The caller must have a read-only lock on the document before calling this method.
old-location: tsf\itextstoreanchor_gettextext.htm
tech.root: TSF
ms.assetid: b8e21544-e5d2-4048-93aa-82a87562a70a
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetTextExt, GetTextExt method [Text Services Framework], GetTextExt method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetTextExt method, ITextStoreAnchor.GetTextExt, ITextStoreAnchor::GetTextExt, textstor/ITextStoreAnchor::GetTextExt, tsf.itextstoreanchor_gettextext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreAnchor.GetTextExt
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchor::GetTextExt


## -description


The <b>ITextStoreAnchor::GetTextExt</b> method returns the bounding box, in screen coordinates, of a range of text. The caller must have a read-only lock on the document before calling this method.


## -parameters




### -param vcView [in]

Specifies the context view.


### -param paStart [in]

Specifies the anchor positioned at the start of the range.


### -param paEnd [in]

Specifies the anchor positioned at the end of the range.


### -param prc [out]

Receives the bounding box of the text range in screen coordinates.


### -param pfClipped [out]

Receives a Boolean value that specifies if the text in the bounding box has been clipped. If <b>TRUE</b>, the bounding box contains clipped text and does not include the entire requested text range. The bounding box is clipped because the requested range is not visible.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to obtain a valid interface pointer to the start and/or end anchors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The range specified by the <i>paStart</i> and <i>paEnd</i> parameters extends past the beginning or end of the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
The application has not calculated a text layout. Any further calls will not succeed until the application calls <a href="https://msdn.microsoft.com/22629ca6-5701-4f6f-b797-bb71c8d31da6">ITextStoreAnchorSink::OnLayoutChange</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read-only lock on the document.

</td>
</tr>
</table>
 




## -remarks



If the document window is minimized, or if the specified text is not currently visible, the method returns S_OK with the <i>prc</i> parameter set to {0,0,0,0}.




## -see-also




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/edde0ba7-1d88-4c32-b794-761b66d73507">ITfContextOwner::GetTextExt
      </a>



<a href="https://msdn.microsoft.com/a4ef9180-5568-4e5b-8c37-f750263060d2">ITfContextView::GetTextExt
      </a>
 

 

