---
UID: NF:wmsdkidl.IWMHeaderInfo2.GetCodecInfoCount
title: IWMHeaderInfo2::GetCodecInfoCount (wmsdkidl.h)
author: windows-sdk-content
description: The GetCodecInfoCount method retrieves the number of codecs for which information is available.
old-location: wmformat\iwmheaderinfo2_getcodecinfocount.htm
tech.root: wmformat
ms.assetid: 1f77f362-5cc7-4d12-9b5f-0436d490b46d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCodecInfoCount, GetCodecInfoCount method [windows Media Format], GetCodecInfoCount method [windows Media Format],IWMHeaderInfo2 interface, GetCodecInfoCount method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo2 interface [windows Media Format],GetCodecInfoCount method, IWMHeaderInfo2.GetCodecInfoCount, IWMHeaderInfo2::GetCodecInfoCount, IWMHeaderInfo2GetCodecInfoCount, IWMHeaderInfo3 interface [windows Media Format],GetCodecInfoCount method, IWMHeaderInfo3::GetCodecInfoCount, wmformat.iwmheaderinfo2_getcodecinfocount, wmsdkidl/IWMHeaderInfo2::GetCodecInfoCount, wmsdkidl/IWMHeaderInfo3::GetCodecInfoCount
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
 - qasf.dll
api_name:
 - IWMHeaderInfo2.GetCodecInfoCount
 - IWMHeaderInfo3.GetCodecInfoCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMHeaderInfo2::GetCodecInfoCount


## -description



The <b>GetCodecInfoCount</b> method retrieves the number of codecs for which information is available. The codecs counted are those that were used to encode the streams of the file loaded in the metadata editor, reader, or synchronous reader object to which the <b>IWMHeaderInfo2</b> interface belongs.




## -parameters




### -param pcCodecInfos [out]

Pointer to a count of codecs for which information is available.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Use this method, and <b>GetCodecInfo</b>, to enumerate through the codec information.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798505(v=VS.85).aspx">IWMHeaderInfo2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798506(v=VS.85).aspx">IWMHeaderInfo2::GetCodecInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798508(v=VS.85).aspx">IWMHeaderInfo3</a>
 

 

