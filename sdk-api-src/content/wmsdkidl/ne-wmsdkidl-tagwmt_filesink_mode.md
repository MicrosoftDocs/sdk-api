---
UID: NE:wmsdkidl.tagWMT_FILESINK_MODE
title: tagWMT_FILESINK_MODE
author: windows-sdk-content
description: The WMT_FILESINK_MODE enumeration type defines the types of input accepted by the file sink.
old-location: wmformat\wmt_filesink_mode.htm
old-project: wmformat
ms.assetid: 27846996-1957-4b19-91da-feeef477b06a
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: WMT_FILESINK_MODE, WMT_FILESINK_MODE enumeration [windows Media Format], WMT_FM_FILESINK_DATA_UNITS, WMT_FM_FILESINK_UNBUFFERED, WMT_FM_SINGLE_BUFFERS, tagWMT_FILESINK_MODE, wmformat.wmt_filesink_mode, wmsdkidl/WMT_FILESINK_MODE, wmsdkidl/WMT_FM_FILESINK_DATA_UNITS, wmsdkidl/WMT_FM_FILESINK_UNBUFFERED, wmsdkidl/WMT_FM_SINGLE_BUFFERS
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WMT_FILESINK_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wmsdkidl.h
api_name:
-	WMT_FILESINK_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagWMT_FILESINK_MODE enumeration


## -description



The <b>WMT_FILESINK_MODE</b> enumeration type defines the types of input accepted by the file sink.




## -enum-fields




### -field WMT_FM_SINGLE_BUFFERS

The file sink accepts normal buffers through calls to <a href="https://msdn.microsoft.com/32e52cdb-e7cb-4caf-a202-0d2ff746017c">IWMWriterSink::OnDataUnit</a>. This is the default behavior.


### -field WMT_FM_FILESINK_DATA_UNITS

The file sink accepts data as <a href="https://msdn.microsoft.com/e1deb01f-9f53-4ede-a3e1-13d6dc79adb5">WMT_FILESINK_DATA_UNIT</a> structures delivered by <a href="https://msdn.microsoft.com/1dbcb27b-7588-4475-99fe-3e547d1659d3">IWMWriterFileSink3::OnDataUnitEx</a>.


### -field WMT_FM_FILESINK_UNBUFFERED

The file sink accepts unbuffered data. A call to <a href="https://msdn.microsoft.com/51a9c21b-d301-41e4-a9bc-321a5b2decca">IWMWriterFileSink3::SetUnbufferedIO</a> will succeed.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

