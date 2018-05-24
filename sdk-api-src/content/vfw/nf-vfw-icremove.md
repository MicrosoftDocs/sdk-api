---
UID: NF:vfw.ICRemove
title: ICRemove function
author: windows-driver-content
description: The ICRemove function removes an installed compressor.
old-location: multimedia\icremove.htm
old-project: Multimedia
ms.assetid: c5f2638a-6b75-4e30-8420-94011c73f5bd
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ICRemove, ICRemove function [Windows Multimedia], _win32_ICRemove, multimedia.icremove, vfw/ICRemove
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
-	ICRemove
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
req.product: Windows UI
---

# ICRemove function


## -description



The <b>ICRemove</b> function removes an installed compressor.




## -parameters




### -param fccType

Four-character code indicating the type of data used by the compressor or decompressor. Specify "VIDC" for a video compressor or decompressor.


### -param fccHandler

Four-character code identifying a specific compressor or a number between zero and the number of installed compressors of the type specified by <i>fccType</i>.


### -param wFlags

Reserved; do not use.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

