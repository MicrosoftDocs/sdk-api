---
UID: NF:wmsdkidl.IWMWriterPostViewCallback.AllocateForPostView
title: IWMWriterPostViewCallback::AllocateForPostView method
author: windows-driver-content
description: The AllocateForPostView method allocates a buffer for use in postviewing operations. The application implements this method.
old-location: wmformat\iwmwriterpostviewcallback_allocateforpostview.htm
old-project: wmformat
ms.assetid: e48132c4-b222-4401-99b3-7906c0df4ec1
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AllocateForPostView method [windows Media Format], AllocateForPostView method [windows Media Format], IWMWriterPostViewCallback interface, AllocateForPostView,IWMWriterPostViewCallback.AllocateForPostView, IWMWriterPostViewCallback, IWMWriterPostViewCallback interface [windows Media Format], AllocateForPostView method, IWMWriterPostViewCallback::AllocateForPostView, IWMWriterPostViewCallbackAllocateForPostView, wmformat.iwmwriterpostviewcallback_allocateforpostview, wmsdkidl/IWMWriterPostViewCallback::AllocateForPostView
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
-	Wmsdkidl.h
api_name:
-	IWMWriterPostViewCallback.AllocateForPostView
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterPostViewCallback::AllocateForPostView method


## -description



The <b>AllocateForPostView</b> method allocates a buffer for use in postviewing operations. The application implements this method.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param cbBuffer [in]

Size of <i>ppBuffer</i>, in bytes.


### -param ppBuffer [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface.


### -param pvContext [in]

Generic pointer, for use by the application.


## -returns



This method is implemented by the application. It should return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/987dd3b4-2245-4640-820c-5a9660ab5e37">IWMWriterPostViewCallback Interface</a>
 

 

