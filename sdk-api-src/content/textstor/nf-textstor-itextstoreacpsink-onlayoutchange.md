---
UID: NF:textstor.ITextStoreACPSink.OnLayoutChange
title: ITextStoreACPSink::OnLayoutChange (textstor.h)
author: windows-sdk-content
description: ITextStoreACPSink::OnLayoutChange method
old-location: tsf\itextstoreacpsink_onlayoutchange.htm
tech.root: TSF
ms.assetid: 2018d3ef-892f-46c0-8dd0-3e27a9f2272c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnLayoutChange method, ITextStoreACPSink.OnLayoutChange, ITextStoreACPSink::OnLayoutChange, OnLayoutChange, OnLayoutChange method [Text Services Framework], OnLayoutChange method [Text Services Framework],ITextStoreACPSink interface, _tsf_itextstoreacpsink_onlayoutchange_ref, textstor/ITextStoreACPSink::OnLayoutChange, tsf.itextstoreacpsink_onlayoutchange
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
 - ITextStoreACPSink.OnLayoutChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITextStoreACPSink::OnLayoutChange


## -description




## -parameters




### -param lcode [in]

Contains a <a href="https://docs.microsoft.com/windows/desktop/api/textstor/ne-textstor-__midl___midl_itf_textstor_0000_0000_0002">TsLayoutCode</a> value that defines the type of change.


### -param vcView [in]

Contains an application-defined cookie that identifies the document. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getactiveview">ITextStoreACP::GetActiveView</a>.


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

If a call to <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettextext">ITextStoreACP::GetTextExt</a> or <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getacpfrompoint">ITextStoreACP::GetACPFromPoint</a> returns TS_E_NOLAYOUT because the application has not calculated the layout, the application must call <b>ITextStoreACPSink::OnLayoutChange</b> when the layout is available.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getacpfrompoint">ITextStoreACP::GetACPFromPoint
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getactiveview">ITextStoreACP::GetActiveView
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettextext">ITextStoreACP::GetTextExt
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacpsink">ITextStoreACPSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/ne-textstor-__midl___midl_itf_textstor_0000_0000_0002">TsLayoutCode
      </a>
 

 

