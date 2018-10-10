---
UID: NF:vfw.ICSeqCompressFrameEnd
title: ICSeqCompressFrameEnd function
author: windows-sdk-content
description: The ICSeqCompressFrameEnd function ends sequence compression that was initiated by using the ICSeqCompressFrameStart and ICSeqCompressFrame functions.
old-location: multimedia\icseqcompressframeend.htm
tech.root: Multimedia
ms.assetid: 3fdcd18d-4ee7-4b5a-871d-61316c716e06
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ICSeqCompressFrameEnd, ICSeqCompressFrameEnd function [Windows Multimedia], _win32_ICSeqCompressFrameEnd, multimedia.icseqcompressframeend, vfw/ICSeqCompressFrameEnd
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - ICSeqCompressFrameEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICSeqCompressFrameEnd function


## -description



The <b>ICSeqCompressFrameEnd</b> function ends sequence compression that was initiated by using the <a href="https://msdn.microsoft.com/90103468-fcdc-4c40-b328-29fe467b9039">ICSeqCompressFrameStart</a> and <a href="https://msdn.microsoft.com/6159e455-1e1a-4aa5-9d75-53cd2af2656a">ICSeqCompressFrame</a> functions.




## -parameters




### -param pc

Pointer to a <a href="https://msdn.microsoft.com/b34378cb-ccf0-4d97-a952-1966999e3f65">COMPVARS</a> structure used during sequence compression.


## -returns



This function does not return a value.




## -remarks



When finished with compression, use the <a href="https://msdn.microsoft.com/6d0c9a7d-6458-4330-af74-3f471555cbfc">ICCompressorFree</a> function to release the resources specified by <a href="https://msdn.microsoft.com/b34378cb-ccf0-4d97-a952-1966999e3f65">COMPVARS</a>.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

