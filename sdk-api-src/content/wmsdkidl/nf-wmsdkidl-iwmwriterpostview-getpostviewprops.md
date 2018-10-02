---
UID: NF:wmsdkidl.IWMWriterPostView.GetPostViewProps
title: IWMWriterPostView::GetPostViewProps
author: windows-sdk-content
description: The GetPostViewProps method retrieves the properties for the specified output stream.
old-location: wmformat\iwmwriterpostview_getpostviewprops.htm
tech.root: wmformat
ms.assetid: 39dc32d1-53e5-43b5-bc96-074dc286890e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetPostViewProps, GetPostViewProps method [windows Media Format], GetPostViewProps method [windows Media Format],IWMWriterPostView interface, IWMWriterPostView interface [windows Media Format],GetPostViewProps method, IWMWriterPostView.GetPostViewProps, IWMWriterPostView::GetPostViewProps, IWMWriterPostViewGetPostViewProps, wmformat.iwmwriterpostview_getpostviewprops, wmsdkidl/IWMWriterPostView::GetPostViewProps
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMWriterPostView.GetPostViewProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterPostView::GetPostViewProps


## -description



The <b>GetPostViewProps</b> method retrieves the properties for the specified output stream.




## -parameters




### -param wStreamNumber [in]

<b>WORD</b> containing the stream number.


### -param ppOutput [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps</a> interface.


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
NULL value passed in to <i>ppOutput</i>.

</td>
</tr>
</table>
 




## -remarks



An application can enumerate through the various outputs, and retrieve the output format properties for that data. Manipulating the object retrieved has no effect on the output, unless the application also calls <a href="https://msdn.microsoft.com/e5b92065-fff3-41d2-b263-375ae14869e5">SetPostViewProps</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a5325d1-880b-4d65-96af-9d311dca989b">IWMReader::SetOutputProps</a>



<a href="https://msdn.microsoft.com/1d24dbd6-86df-4a0a-8110-15f6a4c1f31d">IWMWriterPostView Interface</a>
 

 

