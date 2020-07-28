---
UID: NF:wmsdkidl.IWMWriterAdvanced3.SetNonBlocking
title: IWMWriterAdvanced3::SetNonBlocking (wmsdkidl.h)
description: The SetNonBlocking method configures the writer so that the calling thread is not blocked while writing samples.
helpviewer_keywords: ["IWMWriterAdvanced3 interface [windows Media Format]","SetNonBlocking method","IWMWriterAdvanced3.SetNonBlocking","IWMWriterAdvanced3::SetNonBlocking","IWMWriterAdvanced3SetNonBlocking","SetNonBlocking","SetNonBlocking method [windows Media Format]","SetNonBlocking method [windows Media Format]","IWMWriterAdvanced3 interface","wmformat.iwmwriteradvanced3_setnonblocking","wmsdkidl/IWMWriterAdvanced3::SetNonBlocking"]
old-location: wmformat\iwmwriteradvanced3_setnonblocking.htm
tech.root: wmformat
ms.assetid: 4bec5e6c-5f77-433c-95e0-e3df4dba905c
ms.date: 12/05/2018
ms.keywords: IWMWriterAdvanced3 interface [windows Media Format],SetNonBlocking method, IWMWriterAdvanced3.SetNonBlocking, IWMWriterAdvanced3::SetNonBlocking, IWMWriterAdvanced3SetNonBlocking, SetNonBlocking, SetNonBlocking method [windows Media Format], SetNonBlocking method [windows Media Format],IWMWriterAdvanced3 interface, wmformat.iwmwriteradvanced3_setnonblocking, wmsdkidl/IWMWriterAdvanced3::SetNonBlocking
f1_keywords:
- wmsdkidl/IWMWriterAdvanced3.SetNonBlocking
dev_langs:
- c++
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
- IWMWriterAdvanced3.SetNonBlocking
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterAdvanced3::SetNonBlocking


## -description



The <b>SetNonBlocking</b> method configures the writer so that the calling thread is not blocked while writing samples.




## -parameters






## -returns



The method always returns S_OK.




## -remarks



You should use this method only for time-critical threads. After calling <b>SetNonBlocking</b>, it is the responsibility of the calling application to control the amount of data that is queued to the writer. It is possible to queue too much data for the writer to handle, or to take up too many of the resources of the computer. In extreme cases, the encoding session can stop unexpectedly as a result.

This method has no effect when writing from a live source. It is normal for the writer to refrain from blocking the caller's thread in a live encoding situation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3">IWMWriterAdvanced3 Interface</a>
 

 

