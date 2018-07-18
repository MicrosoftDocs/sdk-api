---
UID: NF:wmsdkidl.IWMWriterAdvanced.GetSinkCount
title: IWMWriterAdvanced::GetSinkCount
author: windows-sdk-content
description: The GetSinkCount method retrieves the number of writer sinks associated with the writer object.
old-location: wmformat\iwmwriteradvanced_getsinkcount.htm
old-project: wmformat
ms.assetid: 210c96bc-3659-43e6-acb2-4d9f328e81e0
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetSinkCount, GetSinkCount method [windows Media Format], GetSinkCount method [windows Media Format],IWMWriterAdvanced interface, IWMWriterAdvanced interface [windows Media Format],GetSinkCount method, IWMWriterAdvanced.GetSinkCount, IWMWriterAdvanced::GetSinkCount, IWMWriterAdvancedGetSinkCount, wmformat.iwmwriteradvanced_getsinkcount, wmsdkidl/IWMWriterAdvanced::GetSinkCount
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
 - IWMWriterAdvanced.GetSinkCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterAdvanced::GetSinkCount


## -description



The <b>GetSinkCount</b> method retrieves the number of writer sinks associated with the writer object. To obtain a pointer to an interface of an individual sink, call <a href="https://msdn.microsoft.com/6775eb89-a3af-42d2-b1e3-197abb1fce61">IWMWriterAdvanced::GetSink</a> using a sink number between 0 and one less than the count returned by this method.




## -parameters




### -param pcSinks [out]

DWORD indicating the total number of sinks associated with the writer object.


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
<i>pcSinks</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



If you specify a file by calling <a href="https://msdn.microsoft.com/352cf497-f7d6-41e8-bdbb-c59215b617a3">IWMWriter::SetOutputFilename</a>, the writer object will automatically create a file sink and add it to the writer. That sink will be included in the count retrieved by this method.




## -see-also




<a href="https://msdn.microsoft.com/1b635cd8-6bdd-4592-bfb5-bcdcf7818e18">Enumerating Sinks</a>



<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>



<a href="https://msdn.microsoft.com/6775eb89-a3af-42d2-b1e3-197abb1fce61">IWMWriterAdvanced::GetSink</a>
 

 

