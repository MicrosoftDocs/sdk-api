---
UID: NF:wmsdkidl.IWMWriterPreprocess.EndPreprocessingPass
title: IWMWriterPreprocess::EndPreprocessingPass
author: windows-sdk-content
description: The EndPreprocessingPass method ends a preprocessing pass started with a call to IWMWriterPreprocess::BeginPreprocessingPass.
old-location: wmformat\iwmwriterpreprocess_endpreprocessingpass.htm
old-project: wmformat
ms.assetid: 04ec12fb-946b-46cc-aa3f-515a86b9a217
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: EndPreprocessingPass, EndPreprocessingPass method [windows Media Format], EndPreprocessingPass method [windows Media Format],IWMWriterPreprocess interface, IWMWriterPreprocess interface [windows Media Format],EndPreprocessingPass method, IWMWriterPreprocess.EndPreprocessingPass, IWMWriterPreprocess::EndPreprocessingPass, IWMWriterPreprocessEndPreprocessingPass, wmformat.iwmwriterpreprocess_endpreprocessingpass, wmsdkidl/IWMWriterPreprocess::EndPreprocessingPass
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
-	IWMWriterPreprocess.EndPreprocessingPass
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterPreprocess::EndPreprocessingPass


## -description



The <b>EndPreprocessingPass</b> method ends a preprocessing pass started with a call to <a href="https://msdn.microsoft.com/593aaa1f-b0eb-43a0-bf73-e90225c07cdf">IWMWriterPreprocess::BeginPreprocessingPass</a>.




## -parameters




### -param dwInputNum [in]

<b>DWORD</b> containing the input number for which you want to halt preprocessing.


### -param dwFlags [in]

Reserved. Set to zero.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwInputNum</i> specifies an invalid input number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The writer is not running.

OR

The preprocessor is not started for the specified stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was an error ending the preprocessing path.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/06803639-3f21-4003-a460-16a0b5cc6d6f">IWMWriterPreprocess Interface</a>
 

 

