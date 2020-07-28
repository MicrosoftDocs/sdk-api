---
UID: NF:wmsdkidl.IWMReaderAdvanced2.GetBufferProgress
title: IWMReaderAdvanced2::GetBufferProgress (wmsdkidl.h)
description: The GetBufferProgress method retrieves the percentage of data that has been buffered, and the time remaining to completion.
helpviewer_keywords: ["GetBufferProgress","GetBufferProgress method [windows Media Format]","GetBufferProgress method [windows Media Format]","IWMReaderAdvanced2 interface","IWMReaderAdvanced2 interface [windows Media Format]","GetBufferProgress method","IWMReaderAdvanced2.GetBufferProgress","IWMReaderAdvanced2::GetBufferProgress","IWMReaderAdvanced2GetBufferProgress","wmformat.iwmreaderadvanced2_getbufferprogress","wmsdkidl/IWMReaderAdvanced2::GetBufferProgress"]
old-location: wmformat\iwmreaderadvanced2_getbufferprogress.htm
tech.root: wmformat
ms.assetid: e0419f53-9962-4d81-9153-0538c60861eb
ms.date: 12/05/2018
ms.keywords: GetBufferProgress, GetBufferProgress method [windows Media Format], GetBufferProgress method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced2 interface [windows Media Format],GetBufferProgress method, IWMReaderAdvanced2.GetBufferProgress, IWMReaderAdvanced2::GetBufferProgress, IWMReaderAdvanced2GetBufferProgress, wmformat.iwmreaderadvanced2_getbufferprogress, wmsdkidl/IWMReaderAdvanced2::GetBufferProgress
f1_keywords:
- wmsdkidl/IWMReaderAdvanced2.GetBufferProgress
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
- IWMReaderAdvanced2.GetBufferProgress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced2::GetBufferProgress


## -description



The <b>GetBufferProgress</b> method retrieves the percentage of data that has been buffered, and the time remaining to completion.




## -parameters




### -param pdwPercent [out]

Pointer to a <b>DWORD</b> containing the percentage of data that has been buffered.


### -param pcnsBuffering [out]

Pointer to variable specifying the time remaining, in 100-nanosecond units, until all the buffering is completed.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



To produce meaningful results, this method must be called between the events WMT_BUFFERING_START and WMT_BUFFERING_STOP. If it is called before a WMT_BUFFERING_START event, then both parameters return zero. If it is called after WMT_BUFFERING_STOP but before a subsequent WMT_BUFFERING_START event, this method returns 100 for the percentage and zero for the buffering time, in seconds. WMT_BUFFERING_START events reset the percentage and seconds remaining to zero.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_play_mode">WMT_PLAY_MODE</a>
 

 

