---
UID: NF:textstor.ITextStoreAnchorSink.OnLayoutChange
title: ITextStoreAnchorSink::OnLayoutChange
author: windows-sdk-content
description: The ITextStoreAnchorSink::OnLayoutChange method is called when the layout (on-screen representation) of the document changes.
old-location: tsf\itextstoreanchorsink_onlayoutchange.htm
tech.root: TSF
ms.assetid: 22629ca6-5701-4f6f-b797-bb71c8d31da6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextStoreAnchorSink interface [Text Services Framework],OnLayoutChange method, ITextStoreAnchorSink.OnLayoutChange, ITextStoreAnchorSink::OnLayoutChange, OnLayoutChange, OnLayoutChange method [Text Services Framework], OnLayoutChange method [Text Services Framework],ITextStoreAnchorSink interface, _tsf_itextstoreanchorsink_onlayoutchange_ref, textstor/ITextStoreAnchorSink::OnLayoutChange, tsf.itextstoreanchorsink_onlayoutchange
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
 - ITextStoreAnchorSink.OnLayoutChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchorSink::OnLayoutChange


## -description


The <b>ITextStoreAnchorSink::OnLayoutChange</b> method is called when the layout (on-screen representation) of the document changes.


## -parameters




### -param lcode [in]

Contains a <a href="https://msdn.microsoft.com/879f83ba-211b-49f6-93b2-6cde5f50fc24">TsLayoutCode</a> value that defines the type of change.


### -param vcView [in]

Contains an application-defined cookie that identifies the document. For more information, see <a href="https://msdn.microsoft.com/b1940cac-7295-41c5-bd26-8be1d1fa4da9">ITextStoreAnchor::GetActiveView</a>.


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
</table>
 




## -remarks



A layout change can be in response to a change to the text, font size, window movement, window resizing, or other change that affects the displayed text.

If a call to <a href="https://msdn.microsoft.com/b8e21544-e5d2-4048-93aa-82a87562a70a">ITextStoreAnchor::GetTextExt</a> or <a href="https://msdn.microsoft.com/5567b53e-540e-41ce-b890-f2e4c5b06c57">ITextStoreAnchor::GetAnchorFromPoint</a> returns TS_E_NOLAYOUT because the application has not calculated the layout, the application must call <b>ITextStoreAnchorSink::OnLayoutChange</b> when the layout is available.




## -see-also




<a href="https://msdn.microsoft.com/b1940cac-7295-41c5-bd26-8be1d1fa4da9">ITextStoreAnchor::GetActiveView
      </a>



<a href="https://msdn.microsoft.com/5567b53e-540e-41ce-b890-f2e4c5b06c57">ITextStoreAnchor::GetAnchorFromPoint
      </a>



<a href="https://msdn.microsoft.com/b8e21544-e5d2-4048-93aa-82a87562a70a">ITextStoreAnchor::GetTextExt
      </a>



<a href="https://msdn.microsoft.com/fb96b4fb-864f-4f32-bf7c-cf7f199e552a">ITextStoreAnchorSink</a>



<a href="https://msdn.microsoft.com/879f83ba-211b-49f6-93b2-6cde5f50fc24">TsLayoutCode
      </a>
 

 

