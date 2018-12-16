---
UID: NF:wmsdkidl.IWMWriterPostView.SetPostViewCallback
title: IWMWriterPostView::SetPostViewCallback
author: windows-sdk-content
description: The SetPostViewCallback method specifies the callback interface to use for receiving postview samples.
old-location: wmformat\iwmwriterpostview_setpostviewcallback.htm
tech.root: wmformat
ms.assetid: c2814f32-1787-44a6-8ffc-5d2a9aca8601
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMWriterPostView interface [windows Media Format],SetPostViewCallback method, IWMWriterPostView.SetPostViewCallback, IWMWriterPostView::SetPostViewCallback, IWMWriterPostViewSetPostViewCallback, SetPostViewCallback, SetPostViewCallback method [windows Media Format], SetPostViewCallback method [windows Media Format],IWMWriterPostView interface, wmformat.iwmwriterpostview_setpostviewcallback, wmsdkidl/IWMWriterPostView::SetPostViewCallback
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
 - IWMWriterPostView.SetPostViewCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterPostView::SetPostViewCallback


## -description



The <b>SetPostViewCallback</b> method specifies the callback interface to use for receiving postview samples.




## -parameters




### -param pCallback [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Dd798771(v=VS.85).aspx">IWMWriterPostViewCallback</a> interface.


### -param pvContext [in]

Generic pointer, for use by the application.


## -returns



This method always returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798770(v=VS.85).aspx">IWMWriterPostView Interface</a>
 

 

