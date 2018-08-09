---
UID: NF:wmsdkidl.IWMReaderAccelerator.GetCodecInterface
title: IWMReaderAccelerator::GetCodecInterface
author: windows-sdk-content
description: The GetCodecInterface method is used to retrieve a pointer to the IWMCodecAMVideoAccelerator interface exposed on the decoder DMO.
old-location: wmformat\iwmreaderaccelerator_getcodecinterface.htm
old-project: wmformat
ms.assetid: e38c02bb-335c-4f93-9e98-1a9dc65a37c5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetCodecInterface, GetCodecInterface method [windows Media Format], GetCodecInterface method [windows Media Format],IWMReaderAccelerator interface, IWMReaderAccelerator interface [windows Media Format],GetCodecInterface method, IWMReaderAccelerator.GetCodecInterface, IWMReaderAccelerator::GetCodecInterface, IWMReaderAcceleratorGetCodecInterface, wmformat.iwmreaderaccelerator_getcodecinterface, wmsdkidl/IWMReaderAccelerator::GetCodecInterface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMReaderAccelerator.GetCodecInterface
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAccelerator::GetCodecInterface


## -description



The <b>GetCodecInterface</b> method is used to retrieve a pointer to the <a href="https://msdn.microsoft.com/48cfc4d1-4b79-47a5-9cc9-a1f19d2c0123">IWMCodecAMVideoAccelerator</a> interface exposed on the decoder <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">DMO</a>.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param riid [in]

Reference to the IID of the interface to obtain. The value must be IID_IWMCodecAMVideoAccelerator.


### -param ppvCodecInterface [out]

Address of a pointer that receives the interface specified by <i>riid</i>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The WM Reader has no pointer to the codec.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>



<a href="https://msdn.microsoft.com/cf783b70-4d19-4006-ad0e-e1f883f00b0b">IWMReaderAccelerator Interface</a>
 

 

