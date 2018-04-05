---
UID: NF:wmsdkidl.IWMReader.GetOutputFormatCount
title: IWMReader::GetOutputFormatCount method
author: windows-driver-content
description: The GetOutputFormatCount method is used for determining all possible format types supported by this output media stream on the reader.
old-location: wmformat\iwmreader_getoutputformatcount.htm
old-project: wmformat
ms.assetid: 282c5fb6-6b8a-4a13-8a20-4926c6f68800
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetOutputFormatCount method [windows Media Format], GetOutputFormatCount method [windows Media Format], IWMReader interface, GetOutputFormatCount,IWMReader.GetOutputFormatCount, IWMReader, IWMReader interface [windows Media Format], GetOutputFormatCount method, IWMReader::GetOutputFormatCount, IWMReaderGetOutputFormatCount, wmformat.iwmreader_getoutputformatcount, wmsdkidl/IWMReader::GetOutputFormatCount
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
-	IWMReader.GetOutputFormatCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReader::GetOutputFormatCount method


## -description



The <b>GetOutputFormatCount</b> method is used for determining all possible format types supported by this output media stream on the reader.




## -parameters




### -param dwOutputNumber [in]

<b>DWORD</b> containing the output number.


### -param pcFormats [out]

Pointer to a count of formats.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The number of formats that can be delivered on output is determined by the decoding codec. The Windows Media codecs can deliver media samples for a stream in a number of formats. For example, the Windows Media Video 9 codec can deliver samples as bitmapped images or as <a href="wmformat_glossary.htm">YUV</a> images with varying properties to suit your needs.

Every compressed media type has a default output format determined by the codec. You can obtain the properties of the default output format by calling <a href="https://msdn.microsoft.com/8958abd0-cc2b-4d02-a831-c998d468fb06">IWMReader::GetOutputProps</a>.

This method is synchronous and does not result in any messages being sent to the status callback.




## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/e73d13b9-3fca-4de1-b89d-5cacc6311cd3">IWMReader::GetOutputFormat</a>
 

 

