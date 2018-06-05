---
UID: NF:wmsdkidl.IWMReaderCallbackAdvanced.AllocateForOutput
title: IWMReaderCallbackAdvanced::AllocateForOutput
author: windows-sdk-content
description: The AllocateForOutput method allocates user-created buffers for samples delivered to IWMReaderCallback::OnSample. For more information about allocating your own buffers, see User Allocated Sample Support.
old-location: wmformat\iwmreadercallbackadvanced_allocateforoutput.htm
old-project: wmformat
ms.assetid: bd7340c9-9380-4dba-b8ac-2a616ce9949f
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: AllocateForOutput, AllocateForOutput method [windows Media Format], AllocateForOutput method [windows Media Format],IWMReaderCallbackAdvanced interface, IWMReaderCallbackAdvanced interface [windows Media Format],AllocateForOutput method, IWMReaderCallbackAdvanced.AllocateForOutput, IWMReaderCallbackAdvanced::AllocateForOutput, IWMReaderCallbackAdvancedAllocateForOutput, wmformat.iwmreadercallbackadvanced_allocateforoutput, wmsdkidl/IWMReaderCallbackAdvanced::AllocateForOutput
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmsdkidl.h
api_name:
-	IWMReaderCallbackAdvanced.AllocateForOutput
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderCallbackAdvanced::AllocateForOutput


## -description



The <b>AllocateForOutput</b> method allocates user-created buffers for samples delivered to <a href="https://msdn.microsoft.com/0f6e4d4f-4295-44ff-95bc-e683bdbab8e0">IWMReaderCallback::OnSample</a>. For more information about allocating your own buffers, see <a href="https://msdn.microsoft.com/c747139e-e157-4ea0-9132-256dc70e2b15">User Allocated Sample Support</a>.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param cbBuffer [in]

Size of the buffer, in bytes.


### -param ppBuffer [out]

If the method succeeds, returns a pointer to a pointer to an <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface.


### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="https://msdn.microsoft.com/485844c6-7a84-4a0d-827d-060d8caef6cc">IWMReader::Start</a> method.


## -returns



To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



An extended version of this method called <a href="https://msdn.microsoft.com/e2e4881b-2186-47c9-b74e-3a59a9fac7c9">AllocateForOutputEx</a> exists in the <a href="https://msdn.microsoft.com/be727c7b-b252-44db-825b-5c683e551fd2">IWMReaderAllocatorEx</a> interface.

When allocating buffers, you can use whatever logic suits your application. Typically, applications initialize a pool of buffers for the file or a pool of buffers for each stream or output. When the application is done with a sample, the buffer is put back into the pool for use.

You can determine the size needed to hold the largest sample of an output by calling <a href="https://msdn.microsoft.com/ad21ab6e-c7af-4293-8920-05db62b9f7ef">IWMReaderAdvanced::GetMaxOutputSampleSize</a>. This is the size you should make the samples in the pool used for the output.

When you allocate a sample in your implementation of this method, you should call <a href="https://msdn.microsoft.com/3f0e8d8a-efc7-4f1b-8a42-7907439ed8af">INSSBuffer::SetLength</a> to set the length of the buffer to the length passed by the reader in the <i>cbBuffer</i> parameter. If you do not set the current length on the buffer, the reader may encounter an error.




## -see-also




<a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced Interface</a>
 

 

