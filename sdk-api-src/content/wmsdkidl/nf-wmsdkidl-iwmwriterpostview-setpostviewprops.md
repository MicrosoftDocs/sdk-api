---
UID: NF:wmsdkidl.IWMWriterPostView.SetPostViewProps
title: IWMWriterPostView::SetPostViewProps
author: windows-sdk-content
description: The SetPostViewProps method specifies the format for the specified output stream.
old-location: wmformat\iwmwriterpostview_setpostviewprops.htm
tech.root: wmformat
ms.assetid: e5b92065-fff3-41d2-b263-375ae14869e5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMWriterPostView interface [windows Media Format],SetPostViewProps method, IWMWriterPostView.SetPostViewProps, IWMWriterPostView::SetPostViewProps, IWMWriterPostViewSetPostViewProps, SetPostViewProps, SetPostViewProps method [windows Media Format], SetPostViewProps method [windows Media Format],IWMWriterPostView interface, wmformat.iwmwriterpostview_setpostviewprops, wmsdkidl/IWMWriterPostView::SetPostViewProps
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
 - IWMWriterPostView.SetPostViewProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterPostView::SetPostViewProps


## -description



The <b>SetPostViewProps</b> method specifies the format for the specified output stream.




## -parameters




### -param wStreamNumber [in]

<b>WORD</b> containing the stream number.


### -param pOutput [in]

Pointer to an <a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps</a> interface.


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
<dt><b>NS_E_INVALID_STREAM</b></dt>
</dl>
</td>
<td width="60%">
The stream number specified by <i>wStreamNumber</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to create an internal structure.

</td>
</tr>
</table>
 




## -remarks



It is not possible to resize the video output using postview properties.

<b>SetPostViewProps</b> fails if <a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">IWMWriter::BeginWriting</a> has been called. If any postview properties need to be changed, this should be done before calling <b>BeginWriting</b>.




## -see-also




<a href="https://msdn.microsoft.com/1d24dbd6-86df-4a0a-8110-15f6a4c1f31d">IWMWriterPostView Interface</a>



<a href="https://msdn.microsoft.com/39dc32d1-53e5-43b5-bc96-074dc286890e">IWMWriterPostView::GetPostViewProps</a>
 

 

