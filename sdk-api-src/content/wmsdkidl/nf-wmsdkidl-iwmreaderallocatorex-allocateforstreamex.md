---
UID: NF:wmsdkidl.IWMReaderAllocatorEx.AllocateForStreamEx
title: IWMReaderAllocatorEx::AllocateForStreamEx
author: windows-sdk-content
description: The AllocateForStreamEx method allocates a user-created buffer for samples delivered to the IWMReaderCallbackAdvanced::OnStreamSample method.
old-location: wmformat\iwmreaderallocatorex_allocateforstreamex.htm
old-project: wmformat
ms.assetid: bb12f0e1-dc9c-447e-a28d-30c45eb95d09
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: AllocateForStreamEx, AllocateForStreamEx method [windows Media Format], AllocateForStreamEx method [windows Media Format],IWMReaderAllocatorEx interface, IWMReaderAllocatorEx interface [windows Media Format],AllocateForStreamEx method, IWMReaderAllocatorEx.AllocateForStreamEx, IWMReaderAllocatorEx::AllocateForStreamEx, IWMReaderAllocatorExAllocateForStreamEx, wmformat.iwmreaderallocatorex_allocateforstreamex, wmsdkidl/IWMReaderAllocatorEx::AllocateForStreamEx
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmsdkidl.h
api_name:
-	IWMReaderAllocatorEx.AllocateForStreamEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAllocatorEx::AllocateForStreamEx


## -description



The <b>AllocateForStreamEx</b> method allocates a user-created buffer for samples delivered to the <a href="https://msdn.microsoft.com/6bfdd903-a3a4-4ef4-b88a-4d24c9c0f4b8">IWMReaderCallbackAdvanced::OnStreamSample</a> method.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param cbBuffer [in]

Size of <i>ppBuffer</i>, in bytes.


### -param ppBuffer [out]

Pointer to a pointer to an <b>INSSBuffer</b> object.


### -param dwFlags [in]

<b>DWORD</b> containing the relevant flags.

<table>
<tr>
<th>
                  Flag
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WM_SFEX_NOTASYNCPOINT</td>
<td>This flag is the opposite of the WM_SF_CLEANPOINT flag used in other methods of this SDK. It indicates that the point is not a <a href="wmformat_glossary.htm">key frame</a>, or is not a good point to go to during a seek. This inverse definition is used for compatibility with Direct Show.</td>
</tr>
<tr>
<td>WM_SFEX_DATALOSS</td>
<td>Some data has been lost between the previous sample and the sample with the flag set.</td>
</tr>
</table>
 


### -param cnsSampleTime [in]

Specifies the sample time, in 100-nanosecond units.


### -param cnsSampleDuration [in]

Specifies the sample duration, in 100-nanosecond units.


### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="https://msdn.microsoft.com/485844c6-7a84-4a0d-827d-060d8caef6cc">IWMReader::Start</a> method.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method differs from <a href="https://msdn.microsoft.com/82d31f4b-d8a8-4538-be5e-dd9149e3f420">IWMReaderCallbackAdvanced::AllocateForStream</a> in that sample time and duration values can be passed.

When you allocate a sample in your implementation of this method, you should call <a href="https://msdn.microsoft.com/3f0e8d8a-efc7-4f1b-8a42-7907439ed8af">INSSBuffer::SetLength</a> to set the length of the buffer to the length passed by the reader in the <i>cbBuffer</i> parameter. If you do not set the current length on the buffer, the reader may encounter an error.




## -see-also




<a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer Interface</a>



<a href="https://msdn.microsoft.com/be727c7b-b252-44db-825b-5c683e551fd2">IWMReaderAllocatorEx Interface</a>



<a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced Interface</a>
 

 

