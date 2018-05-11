---
UID: NF:wmsdkidl.IWMSyncReader2.SetAllocateForStream
title: IWMSyncReader2::SetAllocateForStream
author: windows-driver-content
description: The SetAllocateForStream method sets a sample allocation callback interface for allocating stream samples.
old-location: wmformat\iwmsyncreader2_setallocateforstream.htm
old-project: wmformat
ms.assetid: ed94977e-e930-4045-a69d-36109e7e21c9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWMSyncReader2 interface [windows Media Format],SetAllocateForStream method, IWMSyncReader2.SetAllocateForStream, IWMSyncReader2::SetAllocateForStream, IWMSyncReader2SetAllocateForStream, SetAllocateForStream, SetAllocateForStream method [windows Media Format], SetAllocateForStream method [windows Media Format],IWMSyncReader2 interface, wmformat.iwmsyncreader2_setallocateforstream, wmsdkidl/IWMSyncReader2::SetAllocateForStream
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
-	IWMSyncReader2.SetAllocateForStream
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader2::SetAllocateForStream


## -description



The <b>SetAllocateForStream</b> method sets a sample allocation callback interface for allocating stream samples. This method enables you to use your own buffers for reading samples. Once set, the synchronous reader will call the <a href="https://msdn.microsoft.com/bb12f0e1-dc9c-447e-a28d-30c45eb95d09">IWMReaderAllocatorEx::AllocateForStreamEx</a> method every time it needs a buffer to hold a stream sample.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param pAllocator [in]

Pointer to an <a href="https://msdn.microsoft.com/be727c7b-b252-44db-825b-5c683e551fd2">IWMReaderAllocatorEx</a> interface implemented in your application.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/da66ef5b-ec92-445c-90ba-5ee89e0def36">Allocating Buffers for File Reading</a>



<a href="https://msdn.microsoft.com/f3db7530-a662-46f1-bc64-1dd4523dc87c">IWMSyncReader2 Interface</a>



<a href="https://msdn.microsoft.com/88f02e2d-2585-4668-869b-d42739c02a5c">IWMSyncReader2::GetAllocateForStream</a>
 

 

