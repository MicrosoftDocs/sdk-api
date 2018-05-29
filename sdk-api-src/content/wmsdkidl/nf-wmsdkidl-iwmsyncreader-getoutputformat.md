---
UID: NF:wmsdkidl.IWMSyncReader.GetOutputFormat
title: IWMSyncReader::GetOutputFormat
author: windows-sdk-content
description: The GetOutputFormat method retrieves the supported formats for a specified output media stream.
old-location: wmformat\iwmsyncreader_getoutputformat.htm
old-project: wmformat
ms.assetid: 7faac9e7-ad5f-42a4-ba6e-562ae973f81b
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetOutputFormat, GetOutputFormat method [windows Media Format], GetOutputFormat method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetOutputFormat method, IWMSyncReader.GetOutputFormat, IWMSyncReader::GetOutputFormat, IWMSyncReaderGetOutputFormat, wmformat.iwmsyncreader_getoutputformat, wmsdkidl/IWMSyncReader::GetOutputFormat
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
-	IWMSyncReader.GetOutputFormat
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader::GetOutputFormat


## -description



The <b>GetOutputFormat</b> method retrieves the supported formats for a specified output media stream.




## -parameters




### -param dwOutputNum




### -param dwFormatNum




### -param ppProps [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/8cf40db5-3902-4c14-b728-98da90567e89">IWMOutputMediaProps</a> interface. This object is created by a successful call to this method.


#### - dwFormatNumber [in]

<b>DWORD</b> containing the format number.


#### - dwOutputNumber [in]

<b>DWORD</b> containing the output number.


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
<i>ppProps</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
No file is open in the synchronous reader.

</td>
</tr>
</table>
 




## -remarks



To enumerate the supported formats for an output media stream, call <a href="https://msdn.microsoft.com/66f66784-791b-4f1b-8ba2-300a4521ce03">GetOutputFormatCount</a> to get the number of formats, and then call <b>GetOutputFormat</b> in succession to get the formats.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>
 

 

