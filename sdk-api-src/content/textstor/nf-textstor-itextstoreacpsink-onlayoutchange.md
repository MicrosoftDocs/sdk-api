---
UID: NF:textstor.ITextStoreACPSink.OnLayoutChange
title: ITextStoreACPSink::OnLayoutChange
author: windows-sdk-content
description: ITextStoreACPSink::OnLayoutChange method
old-location: tsf\itextstoreacpsink_onlayoutchange.htm
old-project: TSF
ms.assetid: 2018d3ef-892f-46c0-8dd0-3e27a9f2272c
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnLayoutChange method, ITextStoreACPSink.OnLayoutChange, ITextStoreACPSink::OnLayoutChange, OnLayoutChange, OnLayoutChange method [Text Services Framework], OnLayoutChange method [Text Services Framework],ITextStoreACPSink interface, _tsf_itextstoreacpsink_onlayoutchange_ref, textstor/ITextStoreACPSink::OnLayoutChange, tsf.itextstoreacpsink_onlayoutchange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TsRunType
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACPSink::OnLayoutChange


## -description




## -parameters




### -param lcode [in]

Contains a <a href="https://msdn.microsoft.com/879f83ba-211b-49f6-93b2-6cde5f50fc24">TsLayoutCode</a> value that defines the type of change.


### -param vcView [in]

Contains an application-defined cookie that identifies the document. For more information, see <a href="https://msdn.microsoft.com/7739674e-9524-4530-900c-6e7facc3254f">ITextStoreACP::GetActiveView</a>.


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

If a call to <a href="https://msdn.microsoft.com/d621e96b-d357-4468-8a89-89445fb1ca9e">ITextStoreACP::GetTextExt</a> or <a href="https://msdn.microsoft.com/b6489391-a19e-405a-a129-f68054088860">ITextStoreACP::GetACPFromPoint</a> returns TS_E_NOLAYOUT because the application has not calculated the layout, the application must call <b>ITextStoreACPSink::OnLayoutChange</b> when the layout is available.




## -see-also




<a href="https://msdn.microsoft.com/b6489391-a19e-405a-a129-f68054088860">
        ITextStoreACP::GetACPFromPoint
      </a>



<a href="https://msdn.microsoft.com/7739674e-9524-4530-900c-6e7facc3254f">
        ITextStoreACP::GetActiveView
      </a>



<a href="https://msdn.microsoft.com/d621e96b-d357-4468-8a89-89445fb1ca9e">
        ITextStoreACP::GetTextExt
      </a>



<a href="https://msdn.microsoft.com/d7e5a04f-7159-436e-a522-4cb63063aeef">ITextStoreACPSink</a>



<a href="https://msdn.microsoft.com/879f83ba-211b-49f6-93b2-6cde5f50fc24">TsLayoutCode
      </a>
 

 

