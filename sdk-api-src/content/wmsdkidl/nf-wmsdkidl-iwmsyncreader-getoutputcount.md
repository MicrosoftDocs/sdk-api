---
UID: NF:wmsdkidl.IWMSyncReader.GetOutputCount
title: IWMSyncReader::GetOutputCount
author: windows-sdk-content
description: The GetOutputCount method retrieves the number of outputs that exist for the file open in the synchronous reader.
old-location: wmformat\iwmsyncreader_getoutputcount.htm
tech.root: wmformat
ms.assetid: fde0a136-6c13-43d9-9969-e1226be60f76
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetOutputCount, GetOutputCount method [windows Media Format], GetOutputCount method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetOutputCount method, IWMSyncReader.GetOutputCount, IWMSyncReader::GetOutputCount, IWMSyncReaderGetOutputCount, wmformat.iwmsyncreader_getoutputcount, wmsdkidl/IWMSyncReader::GetOutputCount
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
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
 - IWMSyncReader.GetOutputCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSyncReader::GetOutputCount


## -description



The <b>GetOutputCount</b> method retrieves the number of outputs that exist for the file open in the synchronous reader.




## -parameters




### -param pcOutputs [out]

Pointer to a <b>DWORD</b> that receives the number of outputs in the file.


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
The <i>pcOutputs</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



To enumerate the outputs, call <b>GetOutputCount</b> to get the number of outputs, and then call <b>GetOutputProps</b>.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>



<a href="https://msdn.microsoft.com/a5e701ea-8b53-4abe-8b78-7c6fb151d80f">IWMSyncReader::GetOutputProps</a>



<a href="https://msdn.microsoft.com/f9f979c4-a15c-4f2a-b63c-7fe776394fdd">Inputs, Streams and Outputs</a>
 

 

