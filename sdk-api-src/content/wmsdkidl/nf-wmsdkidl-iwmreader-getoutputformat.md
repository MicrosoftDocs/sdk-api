---
UID: NF:wmsdkidl.IWMReader.GetOutputFormat
title: IWMReader::GetOutputFormat
author: windows-sdk-content
description: The GetOutputFormat method retrieves the supported formats for a specified output media stream.
old-location: wmformat\iwmreader_getoutputformat.htm
old-project: wmformat
ms.assetid: e73d13b9-3fca-4de1-b89d-5cacc6311cd3
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetOutputFormat, GetOutputFormat method [windows Media Format], GetOutputFormat method [windows Media Format],IWMReader interface, IWMReader interface [windows Media Format],GetOutputFormat method, IWMReader.GetOutputFormat, IWMReader::GetOutputFormat, IWMReaderGetOutputFormat, wmformat.iwmreader_getoutputformat, wmsdkidl/IWMReader::GetOutputFormat
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
 - IWMReader.GetOutputFormat
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

Pointer to a pointer to an <a href="https://msdn.microsoft.com/8cf40db5-3902-4c14-b728-98da90567e89">IWMOutputMediaProps</a> interface. This interface belongs to an output media properties object created by a successful call to this method. The properties exposed by this interface represent formats than can be supported by the specified output; the current properties set for the output can be obtained by calling <a href="https://msdn.microsoft.com/8958abd0-cc2b-4d02-a831-c998d468fb06">IWMReader::GetOutputProps</a>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The Windows Media codecs can deliver media samples for a stream in a number of formats. For example, the Windows Media Video 9 codec can deliver samples in various RGB or <a href="https://docs.microsoft.com/windows/desktop//wmformat/wmformat-glossary">YUV</a> formats. You can use this method in conjunction with <a href="https://msdn.microsoft.com/282c5fb6-6b8a-4a13-8a20-4926c6f68800">IWMReader::GetOutputFormatCount</a> to loop through the available formats and find the one you need.

To use a format returned by this method, you must call <a href="https://msdn.microsoft.com/0a5325d1-880b-4d65-96af-9d311dca989b">IWMReader::SetOutputProps</a>.

This method is synchronous and does not result in any messages being sent to the status callback.




## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>
 

 

