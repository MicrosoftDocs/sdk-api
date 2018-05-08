---
UID: NF:wmsdkidl.IWMWriterPostView.GetPostViewFormatCount
title: IWMWriterPostView::GetPostViewFormatCount
author: windows-driver-content
description: The GetPostViewFormatCount method is used for ascertaining all possible format types supported for the specified stream.
old-location: wmformat\iwmwriterpostview_getpostviewformatcount.htm
old-project: wmformat
ms.assetid: b34b2418-5ae4-49a2-913a-bb4ac604ac4e
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetPostViewFormatCount, GetPostViewFormatCount method [windows Media Format], GetPostViewFormatCount method [windows Media Format],IWMWriterPostView interface, IWMWriterPostView interface [windows Media Format],GetPostViewFormatCount method, IWMWriterPostView.GetPostViewFormatCount, IWMWriterPostView::GetPostViewFormatCount, IWMWriterPostViewGetPostViewFormatCount, wmformat.iwmwriterpostview_getpostviewformatcount, wmsdkidl/IWMWriterPostView::GetPostViewFormatCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMWriterPostView.GetPostViewFormatCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterPostView::GetPostViewFormatCount


## -description



The <b>GetPostViewFormatCount</b> method is used for ascertaining all possible format types supported for the specified stream.




## -parameters




### -param wStreamNumber [in]

<b>WORD</b> containing the stream number.


### -param pcFormats [out]

Pointer to a count of the output formats.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
NULL value passed in to <i>pcFormats</i>.

</td>
</tr>
</table>
 




## -remarks



This method can be used along with <a href="https://msdn.microsoft.com/3636833d-3c96-45d9-bf82-e3ff930c7d9b">GetPostViewFormat</a> to ascertain all possible format types supported by this output on the reader.




## -see-also




<a href="https://msdn.microsoft.com/1d24dbd6-86df-4a0a-8110-15f6a4c1f31d">IWMWriterPostView Interface</a>
 

 

