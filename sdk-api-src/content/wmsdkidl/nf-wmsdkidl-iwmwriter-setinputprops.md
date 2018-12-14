---
UID: NF:wmsdkidl.IWMWriter.SetInputProps
title: IWMWriter::SetInputProps
author: windows-sdk-content
description: The SetInputProps method specifies the media properties of an input stream.
old-location: wmformat\iwmwriter_setinputprops.htm
tech.root: wmformat
ms.assetid: 15084a4d-06e8-4f74-9697-ced794d2cdae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMWriter interface [windows Media Format],SetInputProps method, IWMWriter.SetInputProps, IWMWriter::SetInputProps, IWMWriterSetInputProps, SetInputProps, SetInputProps method [windows Media Format], SetInputProps method [windows Media Format],IWMWriter interface, wmformat.iwmwriter_setinputprops, wmsdkidl/IWMWriter::SetInputProps
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
 - IWMWriter.SetInputProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriter::SetInputProps


## -description



The <b>SetInputProps</b> method specifies the media properties of an input stream.




## -parameters




### -param dwInputNum [in]

<b>DWORD</b> containing the input number.


### -param pInput [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Dd757209(v=VS.85).aspx">IWMInputMediaProps</a> interface. See Remarks.


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
<i>dwInputNum</i> is greater than the highest index number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

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



Manipulating the <b>IWMInputMediaProps</b> object has no effect on the writer until the application calls this method to configure the input.

Specify <b>NULL</b> for <i>pInput</i> if the input contains compressed samples that will be written directly to the new stream (using <a href="https://msdn.microsoft.com/en-us/library/Dd798741(v=VS.85).aspx">IWMWriterAdvanced::WriteStreamSample</a>) without being recompressed.




## -see-also




<a href="https://msdn.microsoft.com/44c4ed7e-b35e-4ab5-9975-021f343dab6a">Assigning Input Formats</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798719(v=VS.85).aspx">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757477(v=VS.85).aspx">IWMWriter::GetInputCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757482(v=VS.85).aspx">IWMWriter::GetInputProps</a>
 

 

