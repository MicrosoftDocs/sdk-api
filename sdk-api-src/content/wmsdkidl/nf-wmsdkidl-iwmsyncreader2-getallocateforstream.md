---
UID: NF:wmsdkidl.IWMSyncReader2.GetAllocateForStream
title: IWMSyncReader2::GetAllocateForStream
author: windows-sdk-content
description: The GetAllocateForStream method retrieves an interface for allocating stream samples.
old-location: wmformat\iwmsyncreader2_getallocateforstream.htm
tech.root: wmformat
ms.assetid: 88f02e2d-2585-4668-869b-d42739c02a5c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetAllocateForStream, GetAllocateForStream method [windows Media Format], GetAllocateForStream method [windows Media Format],IWMSyncReader2 interface, IWMSyncReader2 interface [windows Media Format],GetAllocateForStream method, IWMSyncReader2.GetAllocateForStream, IWMSyncReader2::GetAllocateForStream, IWMSyncReader2GetAllocateForStream, wmformat.iwmsyncreader2_getallocateforstream, wmsdkidl/IWMSyncReader2::GetAllocateForStream
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
 - IWMSyncReader2.GetAllocateForStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsdkidl.h
: 
- IWMSyncReader2.GetAllocateForStream
: 
---

# IWMSyncReader2::GetAllocateForStream


## -description



The <b>GetAllocateForStream</b> method retrieves an interface for allocating stream samples.




## -parameters




### -param dwSreamNum [in]

<b>DWORD</b> containing the stream number.


### -param ppAllocator [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/be727c7b-b252-44db-825b-5c683e551fd2">IWMReaderAllocatorEx</a> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f3db7530-a662-46f1-bc64-1dd4523dc87c">IWMSyncReader2 Interface</a>



<a href="https://msdn.microsoft.com/ed94977e-e930-4045-a69d-36109e7e21c9">IWMSyncReader2::SetAllocateForStream</a>
 

 

