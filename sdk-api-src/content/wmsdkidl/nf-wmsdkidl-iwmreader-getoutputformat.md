---
UID: NF:wmsdkidl.IWMReader.GetOutputFormat
title: IWMReader::GetOutputFormat (wmsdkidl.h)
description: The GetOutputFormat method retrieves the supported formats for a specified output media stream.helpviewer_keywords: ["GetOutputFormat","GetOutputFormat method [windows Media Format]","GetOutputFormat method [windows Media Format]","IWMReader interface","IWMReader interface [windows Media Format]","GetOutputFormat method","IWMReader.GetOutputFormat","IWMReader::GetOutputFormat","IWMReaderGetOutputFormat","wmformat.iwmreader_getoutputformat","wmsdkidl/IWMReader::GetOutputFormat"]
old-location: wmformat\iwmreader_getoutputformat.htm
tech.root: wmformat
ms.assetid: e73d13b9-3fca-4de1-b89d-5cacc6311cd3
ms.date: 12/05/2018
ms.keywords: GetOutputFormat, GetOutputFormat method [windows Media Format], GetOutputFormat method [windows Media Format],IWMReader interface, IWMReader interface [windows Media Format],GetOutputFormat method, IWMReader.GetOutputFormat, IWMReader::GetOutputFormat, IWMReaderGetOutputFormat, wmformat.iwmreader_getoutputformat, wmsdkidl/IWMReader::GetOutputFormat
f1_keywords:
- wmsdkidl/IWMReader.GetOutputFormat
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
- IWMReader.GetOutputFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReader::GetOutputFormat


## -description



The <b>GetOutputFormat</b> method retrieves the supported formats for a specified output media stream.




## -parameters




### -param dwOutputNumber [in]

<b>DWORD</b> containing the output number.


### -param dwFormatNumber [in]

<b>DWORD</b> containing the format number.


### -param ppProps [out]

Pointer to a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps</a> interface. This interface belongs to an output media properties object created by a successful call to this method. The properties exposed by this interface represent formats than can be supported by the specified output; the current properties set for the output can be obtained by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops">IWMReader::GetOutputProps</a>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The Windows Media codecs can deliver media samples for a stream in a number of formats. For example, the Windows Media Video 9 codec can deliver samples in various RGB or <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">YUV</a> formats. You can use this method in conjunction with <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount">IWMReader::GetOutputFormatCount</a> to loop through the available formats and find the one you need.

To use a format returned by this method, you must call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops">IWMReader::SetOutputProps</a>.

This method is synchronous and does not result in any messages being sent to the status callback.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>
 

 

