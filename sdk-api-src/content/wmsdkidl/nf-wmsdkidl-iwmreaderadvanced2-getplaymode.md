---
UID: NF:wmsdkidl.IWMReaderAdvanced2.GetPlayMode
title: IWMReaderAdvanced2::GetPlayMode
author: windows-sdk-content
description: The GetPlayMode method retrieves the current play mode.
old-location: wmformat\iwmreaderadvanced2_getplaymode.htm
tech.root: wmformat
ms.assetid: 45c7e2c2-fff4-41a9-b5ce-76d8d6257e77
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetPlayMode, GetPlayMode method [windows Media Format], GetPlayMode method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced2 interface [windows Media Format],GetPlayMode method, IWMReaderAdvanced2.GetPlayMode, IWMReaderAdvanced2::GetPlayMode, IWMReaderAdvanced2GetPlayMode, wmformat.iwmreaderadvanced2_getplaymode, wmsdkidl/IWMReaderAdvanced2::GetPlayMode
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
 - IWMReaderAdvanced2.GetPlayMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsdkidl.h
: 
- IWMReaderAdvanced2.GetPlayMode
: 
---

# IWMReaderAdvanced2::GetPlayMode


## -description



The <b>GetPlayMode</b> method retrieves the current play mode.




## -parameters




### -param pMode [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/da47fc9f-7762-4f92-8857-44a75a4cd00b">WMT_PLAY_MODE</a> enumeration type.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Before a file is opened, this method returns the play mode the reader will use to open a file. The default setting is auto-select (the reader picks the mode). After a file is opened, this method returns the actual mode used to play the file. For an asynchronous <b>Open</b> request, the actual mode can be obtained after receiving the WMT_OPENED status message.

For more information, see the Remarks section of <a href="https://msdn.microsoft.com/d1b20a0c-fedf-46d4-a76b-7596dcf8fcf8">IWMReaderAdvanced2::SetPlayMode</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>
 

 

