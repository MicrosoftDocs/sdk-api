---
UID: NF:vfw.ICInfo
title: ICInfo function
author: windows-driver-content
description: The ICInfo function retrieves information about specific installed compressors or enumerates the installed compressors.
old-location: multimedia\icinfo.htm
old-project: Multimedia
ms.assetid: 755ff010-3edc-4e13-9c8f-104a6d1f590a
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ICInfo, ICInfo function [Windows Multimedia], _win32_ICInfo, multimedia.icinfo, vfw/ICInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msvfw32.dll
api_name:
-	ICInfo
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
req.product: Windows UI
---

# ICInfo function


## -description



The <b>ICInfo</b> function retrieves information about specific installed compressors or enumerates the installed compressors.




## -parameters




### -param fccType

Four-character code indicating the type of compressor. Specify zero to match all compressor types.


### -param fccHandler

Four-character code identifying a specific compressor or a number between zero and the number of installed compressors of the type specified by <i>fccType</i>.


### -param lpicinfo

Pointer to a <a href="https://msdn.microsoft.com/5faf7022-6dc8-475c-8f5a-721bc5b6afee">ICINFO</a> structure to return information about the compressor.


## -returns



Returns <b>TRUE</b> if successful or an error otherwise.




## -remarks



To enumerate the compressors or decompressors, specify an integer for <i>fccHandler</i>. This function returns information for integers between zero and the number of installed compressors or decompressors of the type specified for <i>fccType</i>.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

