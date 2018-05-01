---
UID: NF:wmsdkidl.IWMSyncReader2.GetAllocateForOutput
title: IWMSyncReader2::GetAllocateForOutput method
author: windows-driver-content
description: The GetAllocateForOutput method retrieves an interface for allocating output samples.
old-location: wmformat\iwmsyncreader2_getallocateforoutput.htm
old-project: wmformat
ms.assetid: aef68130-57a8-4bb6-8091-8ee2c75bdf76
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetAllocateForOutput method [windows Media Format], GetAllocateForOutput method [windows Media Format], IWMSyncReader2 interface, GetAllocateForOutput,IWMSyncReader2.GetAllocateForOutput, IWMSyncReader2, IWMSyncReader2 interface [windows Media Format], GetAllocateForOutput method, IWMSyncReader2::GetAllocateForOutput, IWMSyncReader2GetAllocateForOutput, wmformat.iwmsyncreader2_getallocateforoutput, wmsdkidl/IWMSyncReader2::GetAllocateForOutput
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
-	IWMSyncReader2.GetAllocateForOutput
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader2::GetAllocateForOutput method


## -description



The <b>GetAllocateForOutput</b> method retrieves an interface for allocating output samples.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param ppAllocator [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/be727c7b-b252-44db-825b-5c683e551fd2">IWMReaderAllocatorEx</a> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f3db7530-a662-46f1-bc64-1dd4523dc87c">IWMSyncReader2 Interface</a>



<a href="https://msdn.microsoft.com/2f0c754e-f09c-472f-8f40-3fcd0fb29c48">IWMSyncReader2::SetAllocateForOutput</a>
 

 

