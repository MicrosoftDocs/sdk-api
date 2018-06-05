---
UID: NF:wmsdkidl.IWMSyncReader2.SetRangeByTimecode
title: IWMSyncReader2::SetRangeByTimecode
author: windows-sdk-content
description: The SetRangeByTimecode method sets a starting and ending time, based on SMPTE time codes, for playback of a file.
old-location: wmformat\iwmsyncreader2_setrangebytimecode.htm
old-project: wmformat
ms.assetid: 304564b1-6ae3-4e1c-bea9-7a49c522a914
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMSyncReader2 interface [windows Media Format],SetRangeByTimecode method, IWMSyncReader2.SetRangeByTimecode, IWMSyncReader2::SetRangeByTimecode, IWMSyncReader2SetRangeByTimecode, SetRangeByTimecode, SetRangeByTimecode method [windows Media Format], SetRangeByTimecode method [windows Media Format],IWMSyncReader2 interface, wmformat.iwmsyncreader2_setrangebytimecode, wmsdkidl/IWMSyncReader2::SetRangeByTimecode
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
-	IWMSyncReader2.SetRangeByTimecode
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader2::SetRangeByTimecode


## -description



The <b>SetRangeByTimecode</b> method sets a starting and ending time, based on SMPTE time codes, for playback of a file.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param pStart [in]

Pointer to a <a href="https://msdn.microsoft.com/039c352c-d1f0-443f-acef-f730e949725c">WMT_TIMECODE_EXTENSION_DATA</a> structure containing the starting time code.


### -param pEnd [in]

Pointer to a <b>WMT_TIMECODE_EXTENSION_DATA</b> structure containing the ending time code.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



For the method to succeed, the file must be indexed by SMPTE time code.

If the call is successful, all streams are synchronized to the same position based on presentation time.




## -see-also




<a href="https://msdn.microsoft.com/f3db7530-a662-46f1-bc64-1dd4523dc87c">IWMSyncReader2 Interface</a>
 

 

