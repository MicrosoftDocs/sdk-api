---
UID: NF:wmsdkidl.IWMReader.GetOutputProps
title: IWMReader::GetOutputProps (wmsdkidl.h)
description: The GetOutputProps method retrieves the current properties of an uncompressed output stream.helpviewer_keywords: ["GetOutputProps","GetOutputProps method [windows Media Format]","GetOutputProps method [windows Media Format]","IWMReader interface","IWMReader interface [windows Media Format]","GetOutputProps method","IWMReader.GetOutputProps","IWMReader::GetOutputProps","IWMReaderGetOutputProps","wmformat.iwmreader_getoutputprops","wmsdkidl/IWMReader::GetOutputProps"]
old-location: wmformat\iwmreader_getoutputprops.htm
tech.root: wmformat
ms.assetid: 8958abd0-cc2b-4d02-a831-c998d468fb06
ms.date: 12/05/2018
ms.keywords: GetOutputProps, GetOutputProps method [windows Media Format], GetOutputProps method [windows Media Format],IWMReader interface, IWMReader interface [windows Media Format],GetOutputProps method, IWMReader.GetOutputProps, IWMReader::GetOutputProps, IWMReaderGetOutputProps, wmformat.iwmreader_getoutputprops, wmsdkidl/IWMReader::GetOutputProps
f1_keywords:
- wmsdkidl/IWMReader.GetOutputProps
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
- IWMReader.GetOutputProps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReader::GetOutputProps


## -description



The <b>GetOutputProps</b> method retrieves the current properties of an uncompressed output stream.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param ppOutput [out]

Pointer to a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps</a> interface. This interface belongs to an output media properties object created by a successful call to this method. Any changes made to the output media properties object will have no effect on the output of the reader unless you pass this interface in a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops">IWMReader::SetOutputProps</a>.


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
The <i>ppOutput</i> parameter is <b>NULL</b>, or the <i>dwOutputNum</i> parameter is greater than the number of outputs.

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



The Windows Media codecs can deliver media samples for a stream in a number of formats. For example, the Windows Media Video 9 codec can deliver samples as bitmapped images or as <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">YUV</a> images with varying properties to suit your needs. When you load a file the output properties are set to the default for compressed media type in the stream associated with the output. You can examine the possible output formats by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount">IWMReader::GetOutputFormatCount</a> to get the total number of possible formats and then calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat">IWMReader::GetOutputFormat</a> for each.

This method is synchronous and does not result in any messages being sent to the status callback.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>
 

 

