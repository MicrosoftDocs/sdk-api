---
UID: NF:wmsdkidl.IWMSyncReader.Open
title: IWMSyncReader::Open
author: windows-sdk-content
description: The Open method opens a file for reading. Unlike IWMReader::Open, this method is a synchronous call.
old-location: wmformat\iwmsyncreader_open.htm
old-project: wmformat
ms.assetid: dab1a9c4-487c-4b20-909e-05f3504698f5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMSyncReader interface [windows Media Format],Open method, IWMSyncReader.Open, IWMSyncReader::Open, IWMSyncReaderOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMSyncReader interface, wmformat.iwmsyncreader_open, wmsdkidl/IWMSyncReader::Open
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
 - IWMSyncReader.Open
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader::Open


## -description



The <b>Open</b> method opens a file for reading. Unlike <a href="https://msdn.microsoft.com/ab5b7f9e-b647-4121-abb3-2c9deb1f50cc">IWMReader::Open</a>, this method is a synchronous call.




## -parameters




### -param pwszFilename [in]

Pointer to a wide-character null-terminated string containing the file name to open. This must be a valid file name with an ASF file extension or an MP3 file name.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The synchronous reader does not support streaming media. Passing a URL as <i>pwszFilename</i> results in an error.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>



<a href="https://msdn.microsoft.com/98f5a44f-dc34-4732-b497-5528de6af1c3">IWMSyncReader::Close</a>



<a href="https://msdn.microsoft.com/ef42495a-2565-4925-882e-c3c42f9d418b">IWMSyncReader::OpenStream</a>
 

 

