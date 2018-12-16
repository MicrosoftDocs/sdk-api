---
UID: NF:wmsdkidl.IWMSyncReader.Open
title: IWMSyncReader::Open
author: windows-sdk-content
description: The Open method opens a file for reading. Unlike IWMReader::Open, this method is a synchronous call.
old-location: wmformat\iwmsyncreader_open.htm
tech.root: wmformat
ms.assetid: dab1a9c4-487c-4b20-909e-05f3504698f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMSyncReader interface [windows Media Format],Open method, IWMSyncReader.Open, IWMSyncReader::Open, IWMSyncReaderOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMSyncReader interface, wmformat.iwmsyncreader_open, wmsdkidl/IWMSyncReader::Open
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
 - IWMSyncReader.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSyncReader::Open


## -description



The <b>Open</b> method opens a file for reading. Unlike <a href="https://msdn.microsoft.com/en-us/library/Dd743597(v=VS.85).aspx">IWMReader::Open</a>, this method is a synchronous call.




## -parameters




### -param pwszFilename [in]

Pointer to a wide-character null-terminated string containing the file name to open. This must be a valid file name with an ASF file extension or an MP3 file name.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The synchronous reader does not support streaming media. Passing a URL as <i>pwszFilename</i> results in an error.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798576(v=VS.85).aspx">IWMSyncReader Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798584(v=VS.85).aspx">IWMSyncReader::Close</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798598(v=VS.85).aspx">IWMSyncReader::OpenStream</a>
 

 

