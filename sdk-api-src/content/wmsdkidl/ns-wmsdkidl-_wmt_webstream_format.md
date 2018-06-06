---
UID: NS:wmsdkidl._WMT_WEBSTREAM_FORMAT
title: "_WMT_WEBSTREAM_FORMAT"
author: windows-sdk-content
description: The WMT_WEBSTREAM_FORMAT structure contains information about a Web stream. This structure is used as the pbFormat member of the WM_MEDIA_TYPE structure for Web streams.
old-location: wmformat\wmt_webstream_format.htm
old-project: wmformat
ms.assetid: 3a392b33-6c2b-4465-86b4-6614940d7383
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: WMT_WEBSTREAM_FORMAT, WMT_WEBSTREAM_FORMAT structure [windows Media Format], _WMT_WEBSTREAM_FORMAT, wmformat.wmt_webstream_format, wmsdkidl/WMT_WEBSTREAM_FORMAT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: WMT_WEBSTREAM_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_WEBSTREAM_FORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WMT_WEBSTREAM_FORMAT structure


## -description



The <b>WMT_WEBSTREAM_FORMAT</b> structure contains information about a Web stream. This structure is used as the <b>pbFormat</b> member of the <a href="https://msdn.microsoft.com/37a9ac59-e152-47e1-96ee-b816cd645936">WM_MEDIA_TYPE</a> structure for Web streams.




## -struct-fields




### -field cbSize

<b>WORD</b> containing the size of the structure, in bytes.


### -field cbSampleHeaderFixedData

<b>WORD</b> containing the size of Web stream sample header, in bytes.


### -field wVersion

<b>WORD</b> containing the version number. Set to 1 for streams created with the Windows Media Format 9 Series SDK.


### -field wReserved

<b>WORD</b>. Reserved.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

