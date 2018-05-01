---
UID: NF:wmsdkidl.IWMWriterFileSink3.OnDataUnitEx
title: IWMWriterFileSink3::OnDataUnitEx method
author: windows-driver-content
description: The OnDataUnitEx method is called when the writer has finished sending a data unit.
old-location: wmformat\iwmwriterfilesink3_ondataunitex.htm
old-project: wmformat
ms.assetid: 1dbcb27b-7588-4475-99fe-3e547d1659d3
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMWriterFileSink3, IWMWriterFileSink3 interface [windows Media Format], OnDataUnitEx method, IWMWriterFileSink3::OnDataUnitEx, IWMWriterFileSink3OnDataUnitEx, OnDataUnitEx method [windows Media Format], OnDataUnitEx method [windows Media Format], IWMWriterFileSink3 interface, OnDataUnitEx,IWMWriterFileSink3.OnDataUnitEx, wmformat.iwmwriterfilesink3_ondataunitex, wmsdkidl/IWMWriterFileSink3::OnDataUnitEx
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
-	IWMWriterFileSink3.OnDataUnitEx
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterFileSink3::OnDataUnitEx method


## -description



The <b>OnDataUnitEx</b> method is called when the writer has finished sending a data unit.



<b>OnDataUnitEx</b> is an enhanced version of <a href="https://msdn.microsoft.com/32e52cdb-e7cb-4caf-a202-0d2ff746017c">IWMWriterSink::OnDataUnit</a>. The difference between these two methods is that <b>OnDataUnitEx</b> delivers very granular data unit information. You can examine individual payload headers, payload data fragments, and the packet header.


## -parameters




### -param pFileSinkDataUnit [in]

Pointer to a <a href="https://msdn.microsoft.com/e1deb01f-9f53-4ede-a3e1-13d6dc79adb5">WMT_FILESINK_DATA_UNIT</a> structure containing the data unit information.


## -returns



This method always returns S_OK.




## -remarks



Applications do not call this method. If you are implementing the <b>IWMWriterFileSink3</b> interface on a custom sink, you have the option of implementing this method. If you do so, your implementation of <a href="https://msdn.microsoft.com/a8a7003e-e59f-451c-9f45-75d6d094a03b">GetMode</a> should return WMT_FM_FILESINK_DATA_UNITS.




## -see-also




<a href="https://msdn.microsoft.com/67f418c8-184d-46f0-8939-69194c7e7a50">IWMWriterFileSink3 Interface</a>
 

 

