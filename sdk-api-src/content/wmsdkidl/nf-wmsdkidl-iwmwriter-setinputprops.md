---
UID: NF:wmsdkidl.IWMWriter.SetInputProps
title: IWMWriter::SetInputProps (wmsdkidl.h)
description: The SetInputProps method specifies the media properties of an input stream.helpviewer_keywords: ["IWMWriter interface [windows Media Format]","SetInputProps method","IWMWriter.SetInputProps","IWMWriter::SetInputProps","IWMWriterSetInputProps","SetInputProps","SetInputProps method [windows Media Format]","SetInputProps method [windows Media Format]","IWMWriter interface","wmformat.iwmwriter_setinputprops","wmsdkidl/IWMWriter::SetInputProps"]
old-location: wmformat\iwmwriter_setinputprops.htm
tech.root: wmformat
ms.assetid: 15084a4d-06e8-4f74-9697-ced794d2cdae
ms.date: 12/05/2018
ms.keywords: IWMWriter interface [windows Media Format],SetInputProps method, IWMWriter.SetInputProps, IWMWriter::SetInputProps, IWMWriterSetInputProps, SetInputProps, SetInputProps method [windows Media Format], SetInputProps method [windows Media Format],IWMWriter interface, wmformat.iwmwriter_setinputprops, wmsdkidl/IWMWriter::SetInputProps
f1_keywords:
- wmsdkidl/IWMWriter.SetInputProps
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriter::SetInputProps


## -description



The <b>SetInputProps</b> method specifies the media properties of an input stream.




## -parameters




### -param dwInputNum [in]

<b>DWORD</b> containing the input number.


### -param pInput [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops">IWMInputMediaProps</a> interface. See Remarks.


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

Specify <b>NULL</b> for <i>pInput</i> if the input contains compressed samples that will be written directly to the new stream (using <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample">IWMWriterAdvanced::WriteStreamSample</a>) without being recompressed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/assigning-input-formats">Assigning Input Formats</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount">IWMWriter::GetInputCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops">IWMWriter::GetInputProps</a>
 

 

