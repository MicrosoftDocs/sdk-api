---
UID: NE:wmsdkidl.tagWMT_FILESINK_MODE
title: WMT_FILESINK_MODE (wmsdkidl.h)
author: windows-sdk-content
description: The WMT_FILESINK_MODE enumeration type defines the types of input accepted by the file sink.
old-location: wmformat\wmt_filesink_mode.htm
tech.root: wmformat
ms.assetid: 27846996-1957-4b19-91da-feeef477b06a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WMT_FILESINK_MODE, WMT_FILESINK_MODE enumeration [windows Media Format], WMT_FM_FILESINK_DATA_UNITS, WMT_FM_FILESINK_UNBUFFERED, WMT_FM_SINGLE_BUFFERS, wmformat.wmt_filesink_mode, wmsdkidl/WMT_FILESINK_MODE, wmsdkidl/WMT_FM_FILESINK_DATA_UNITS, wmsdkidl/WMT_FM_FILESINK_UNBUFFERED, wmsdkidl/WMT_FM_SINGLE_BUFFERS
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_FILESINK_MODE
product: Windows
targetos: Windows
req.typenames: WMT_FILESINK_MODE
req.redist: 
---

# WMT_FILESINK_MODE enumeration


## -description



The <b>WMT_FILESINK_MODE</b> enumeration type defines the types of input accepted by the file sink.




## -enum-fields




### -field WMT_FM_SINGLE_BUFFERS

The file sink accepts normal buffers through calls to <a href="https://msdn.microsoft.com/en-us/library/Dd757470(v=VS.85).aspx">IWMWriterSink::OnDataUnit</a>. This is the default behavior.


### -field WMT_FM_FILESINK_DATA_UNITS

The file sink accepts data as <a href="https://msdn.microsoft.com/en-us/library/Dd757841(v=VS.85).aspx">WMT_FILESINK_DATA_UNIT</a> structures delivered by <a href="https://msdn.microsoft.com/en-us/library/Dd798756(v=VS.85).aspx">IWMWriterFileSink3::OnDataUnitEx</a>.


### -field WMT_FM_FILESINK_UNBUFFERED

The file sink accepts unbuffered data. A call to <a href="https://msdn.microsoft.com/en-us/library/Dd798759(v=VS.85).aspx">IWMWriterFileSink3::SetUnbufferedIO</a> will succeed.


## -see-also




<a href="https://msdn.microsoft.com/cd28f608-25ba-44a7-868b-b1cd4dfcfa45">Enumeration Types</a>
 

 

