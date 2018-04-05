---
UID: NF:wmsdkidl.IWMReaderAdvanced2.SetPlayMode
title: IWMReaderAdvanced2::SetPlayMode method
author: windows-driver-content
description: The SetPlayMode method specifies the play mode.
old-location: wmformat\iwmreaderadvanced2_setplaymode.htm
old-project: wmformat
ms.assetid: d1b20a0c-fedf-46d4-a76b-7596dcf8fcf8
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWMReaderAdvanced2, IWMReaderAdvanced2 interface [windows Media Format], SetPlayMode method, IWMReaderAdvanced2::SetPlayMode, IWMReaderAdvanced2SetPlayMode, SetPlayMode method [windows Media Format], SetPlayMode method [windows Media Format], IWMReaderAdvanced2 interface, SetPlayMode,IWMReaderAdvanced2.SetPlayMode, wmformat.iwmreaderadvanced2_setplaymode, wmsdkidl/IWMReaderAdvanced2::SetPlayMode
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
-	IWMReaderAdvanced2.SetPlayMode
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced2::SetPlayMode method


## -description



The <b>SetPlayMode</b> method specifies the play mode.




## -parameters




### -param Mode [in]

Variable containing one member of the <a href="https://msdn.microsoft.com/da47fc9f-7762-4f92-8857-44a75a4cd00b">WMT_PLAY_MODE</a> enumeration type.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The default play mode is WMT_PLAY_MODE_AUTOSELECT, which enables the reader to pick the mode. If the application selects a play mode that is incompatible with the requested URL, an error is returned when the URL is opened. After the asynchronous reply to the <b>Open</b> request is completed, the mode is changed from WMT_PLAY_MODE_AUTOSELECT to the appropriately selected play mode. The play mode cannot be changed after the content has been opened, and returns an error if this is attempted.




## -see-also




<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/45c7e2c2-fff4-41a9-b5ce-76d8d6257e77">IWMReaderAdvanced2::GetPlayMode</a>
 

 

