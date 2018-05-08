---
UID: NF:wmsdkidl.IWMReaderTypeNegotiation.TryOutputProps
title: IWMReaderTypeNegotiation::TryOutputProps
author: windows-driver-content
description: The TryOutputProps method ascertains whether certain changes to the properties of an output are possible.
old-location: wmformat\iwmreadertypenegotiation_tryoutputprops.htm
old-project: wmformat
ms.assetid: 87d16641-3d28-4bad-962b-8ec808cd7877
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMReaderTypeNegotiation interface [windows Media Format],TryOutputProps method, IWMReaderTypeNegotiation.TryOutputProps, IWMReaderTypeNegotiation::TryOutputProps, IWMReaderTypeNegotiationTryOutputProps, TryOutputProps, TryOutputProps method [windows Media Format], TryOutputProps method [windows Media Format],IWMReaderTypeNegotiation interface, wmformat.iwmreadertypenegotiation_tryoutputprops, wmsdkidl/IWMReaderTypeNegotiation::TryOutputProps
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderTypeNegotiation.TryOutputProps
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderTypeNegotiation::TryOutputProps


## -description



The <b>TryOutputProps</b> method ascertains whether certain changes to the properties of an output are possible.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param pOutput [in]

Pointer to the <a href="https://msdn.microsoft.com/8cf40db5-3902-4c14-b728-98da90567e89">IWMOutputMediaProps</a> interface of an output media properties object.


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
<i>dwOutputNumber</i> is too large.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_OUTPUT_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
Media type of object is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to complete the task.

</td>
</tr>
</table>
 




## -remarks



This method is usually used to test different output properties to find out if they are possible; for example, to find out whether a video stream can be rendered at a resolution of 320 x 240 pixels in 16-bit color. To perform this testing, call <a href="https://msdn.microsoft.com/8958abd0-cc2b-4d02-a831-c998d468fb06">IWMReader::GetOutputProps</a> to retrieve an <b>IWMOutputMediaProps</b> interface, and alter properties by using that interface. Then test the modified object with the <b>TryOutputProps</b> method. If it returns S_OK, the new properties would work.




## -see-also




<a href="https://msdn.microsoft.com/8cf40db5-3902-4c14-b728-98da90567e89">IWMOutputMediaProps Interface</a>



<a href="https://msdn.microsoft.com/289ca857-5421-47f8-927e-6ca4204a31f9">IWMReaderTypeNegotiation Interface</a>



<a href="https://msdn.microsoft.com/f9f979c4-a15c-4f2a-b63c-7fe776394fdd">Inputs, Streams and Outputs</a>
 

 

