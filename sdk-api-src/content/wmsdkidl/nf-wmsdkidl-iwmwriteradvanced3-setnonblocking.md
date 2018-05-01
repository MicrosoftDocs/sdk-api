---
UID: NF:wmsdkidl.IWMWriterAdvanced3.SetNonBlocking
title: IWMWriterAdvanced3::SetNonBlocking method
author: windows-driver-content
description: The SetNonBlocking method configures the writer so that the calling thread is not blocked while writing samples.
old-location: wmformat\iwmwriteradvanced3_setnonblocking.htm
old-project: wmformat
ms.assetid: 4bec5e6c-5f77-433c-95e0-e3df4dba905c
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMWriterAdvanced3, IWMWriterAdvanced3 interface [windows Media Format], SetNonBlocking method, IWMWriterAdvanced3::SetNonBlocking, IWMWriterAdvanced3SetNonBlocking, SetNonBlocking method [windows Media Format], SetNonBlocking method [windows Media Format], IWMWriterAdvanced3 interface, SetNonBlocking,IWMWriterAdvanced3.SetNonBlocking, wmformat.iwmwriteradvanced3_setnonblocking, wmsdkidl/IWMWriterAdvanced3::SetNonBlocking
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
-	IWMWriterAdvanced3.SetNonBlocking
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterAdvanced3::SetNonBlocking method


## -description



The <b>SetNonBlocking</b> method configures the writer so that the calling thread is not blocked while writing samples.




## -parameters






## -returns



The method always returns S_OK.




## -remarks



You should use this method only for time-critical threads. After calling <b>SetNonBlocking</b>, it is the responsibility of the calling application to control the amount of data that is queued to the writer. It is possible to queue too much data for the writer to handle, or to take up too many of the resources of the computer. In extreme cases, the encoding session can stop unexpectedly as a result.

This method has no effect when writing from a live source. It is normal for the writer to refrain from blocking the caller's thread in a live encoding situation.




## -see-also




<a href="https://msdn.microsoft.com/99f7e4f7-0080-498d-b4f1-960c4955b4db">IWMWriterAdvanced3 Interface</a>
 

 

