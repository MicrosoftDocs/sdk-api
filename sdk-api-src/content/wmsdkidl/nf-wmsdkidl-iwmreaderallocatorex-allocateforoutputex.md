---
UID: NF:wmsdkidl.IWMReaderAllocatorEx.AllocateForOutputEx
title: IWMReaderAllocatorEx::AllocateForOutputEx (wmsdkidl.h)
author: windows-sdk-content
description: The AllocateForOutputEx method allocates a user-created buffer for samples delivered to the IWMReaderCallback::OnSample method.
old-location: wmformat\iwmreaderallocatorex_allocateforoutputex.htm
tech.root: wmformat
ms.assetid: e2e4881b-2186-47c9-b74e-3a59a9fac7c9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AllocateForOutputEx, AllocateForOutputEx method [windows Media Format], AllocateForOutputEx method [windows Media Format],IWMReaderAllocatorEx interface, IWMReaderAllocatorEx interface [windows Media Format],AllocateForOutputEx method, IWMReaderAllocatorEx.AllocateForOutputEx, IWMReaderAllocatorEx::AllocateForOutputEx, IWMReaderAllocatorExAllocateForOutputEx, wmformat.iwmreaderallocatorex_allocateforoutputex, wmsdkidl/IWMReaderAllocatorEx::AllocateForOutputEx
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsdkidl.h
api_name:
 - IWMReaderAllocatorEx.AllocateForOutputEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAllocatorEx::AllocateForOutputEx


## -description



The <b>AllocateForOutputEx</b> method allocates a user-created buffer for samples delivered to the <a href="https://msdn.microsoft.com/en-us/library/Dd743503(v=VS.85).aspx">IWMReaderCallback::OnSample</a> method.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param cbBuffer [in]

Size of <i>ppBuffer</i>, in bytes.


### -param ppBuffer [out]

Pointer to a pointer to an <b>INSSBuffer</b> object.


### -param dwFlags [in]

<b>DWORD</b> containing the relevant flags.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WM_SFEX_NOTASYNCPOINT</td>
<td>This flag is the opposite of the WM_SF_CLEANPOINT flag used in other methods of this SDK. It indicates that the point is not a <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">key frame</a>, or is not a good point to go to during a seek. This inverse definition is used for compatibility with DirectShow.</td>
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

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="https://msdn.microsoft.com/en-us/library/Dd743608(v=VS.85).aspx">IWMReader::Start</a> method.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method differs from <a href="https://msdn.microsoft.com/en-us/library/Dd743495(v=VS.85).aspx">IWMReaderCallbackAdvanced::AllocateForOutput</a> in that sample time and duration values can be passed.

When you allocate a sample in your implementation of this method, you should call <a href="https://msdn.microsoft.com/en-us/library/Dd743263(v=VS.85).aspx">INSSBuffer::SetLength</a> to set the length of the buffer to the length passed by the reader in the <i>cbBuffer</i> parameter. If you do not set the current length on the buffer, the reader may encounter an error.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743243(v=VS.85).aspx">INSSBuffer Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743490(v=VS.85).aspx">IWMReaderAllocatorEx Interface</a>
 

 

