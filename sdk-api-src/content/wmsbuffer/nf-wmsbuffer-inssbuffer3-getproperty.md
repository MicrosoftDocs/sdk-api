---
UID: NF:wmsbuffer.INSSBuffer3.GetProperty
title: INSSBuffer3::GetProperty
author: windows-sdk-content
description: The GetProperty method is used to retrieve a property of the sample in the buffer. Buffer properties are used to pass information along with the sample to the writer object when writing ASF files. Sample properties are GUID values.
old-location: wmformat\inssbuffer3_getproperty.htm
old-project: wmformat
ms.assetid: b7733df5-f764-4996-b324-fa050b1db0af
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetProperty, GetProperty method [windows Media Format], GetProperty method [windows Media Format],INSSBuffer3 interface, INSSBuffer3 interface [windows Media Format],GetProperty method, INSSBuffer3.GetProperty, INSSBuffer3::GetProperty, INSSBuffer3GetProperty, wmformat.inssbuffer3_getproperty, wmsbuffer/INSSBuffer3::GetProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsbuffer.h
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
req.typenames: WMPServices_StreamState
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
-	INSSBuffer3.GetProperty
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# INSSBuffer3::GetProperty


## -description



The <b>GetProperty</b> method is used to retrieve a property of the sample in the buffer. Buffer properties are used to pass information along with the sample to the writer object when writing ASF files. Sample properties are GUID values.




## -parameters




### -param guidBufferProperty [in]

<b>GUID</b> value identifying the property to retrieve. The predefined buffer properties are described in the <a href="https://msdn.microsoft.com/8de2e003-cb21-4be9-bcde-7f5909b6260a">Sample Extension Types</a> section of this documentation. You can also define your own sample extension schemes using your own GUID values.


### -param pvBufferProperty [out]

Pointer to a buffer that will receive the value of the property specified by <i>guidBufferProperty</i>.


### -param pdwBufferPropertySize [in, out]

Pointer to a <b>DWORD</b> value containing the size of the buffer pointed to by <i>pvBufferProperty</i>. If you pass <b>NULL</b> for <i>pvBufferProperty</i>, the method sets the value pointed to by this parameter to the size required to hold the property value. If you pass a non-<b>NULL</b> value for <i>pvBufferProperty</i>, the value pointed to by this parameter must equal the size of the buffer pointed to by <i>pvBufferProperty</i>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwBufferPropertySize</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The property specified as <i>guidBufferProperty</i> is not set in this buffer object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3ebf80d0-b5b0-4024-805d-e0a3855574bf">INSSBuffer3 Interface</a>



<a href="https://msdn.microsoft.com/5aede025-65ae-4615-9511-af22b8c0dc00">INSSBuffer3::SetProperty</a>
 

 

