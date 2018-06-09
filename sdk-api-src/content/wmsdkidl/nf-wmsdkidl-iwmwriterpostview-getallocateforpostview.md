---
UID: NF:wmsdkidl.IWMWriterPostView.GetAllocateForPostView
title: IWMWriterPostView::GetAllocateForPostView
author: windows-sdk-content
description: The GetAllocateForPostView method ascertains whether the application, and not the writer, must supply the buffers.
old-location: wmformat\iwmwriterpostview_getallocateforpostview.htm
old-project: wmformat
ms.assetid: bd17eeec-a1ce-42db-a807-008ca2c4194f
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetAllocateForPostView, GetAllocateForPostView method [windows Media Format], GetAllocateForPostView method [windows Media Format],IWMWriterPostView interface, IWMWriterPostView interface [windows Media Format],GetAllocateForPostView method, IWMWriterPostView.GetAllocateForPostView, IWMWriterPostView::GetAllocateForPostView, IWMWriterPostViewGetAllocateForPostView, wmformat.iwmwriterpostview_getallocateforpostview, wmsdkidl/IWMWriterPostView::GetAllocateForPostView
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMWriterPostView.GetAllocateForPostView
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterPostView::GetAllocateForPostView


## -description



The <b>GetAllocateForPostView</b> method ascertains whether the application, and not the writer, must supply the buffers.




## -parameters




### -param wStreamNumber [in]

<b>WORD</b> containing the stream number.


### -param pfAllocate [out]

Pointer to Boolean value that is True if the application allocates buffers, and False if this is left to the writer.


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
NULL value passed in to <i>pfAllocate</i>.

</td>
</tr>
</table>
 




## -remarks



See the Remarks for <a href="https://msdn.microsoft.com/995bf3fa-3e10-46a2-ad51-55375d6af447">SetAllocateForPostView</a>.




## -see-also




<a href="https://msdn.microsoft.com/1d24dbd6-86df-4a0a-8110-15f6a4c1f31d">IWMWriterPostView Interface</a>
 

 

