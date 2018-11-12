---
UID: NF:vfw.ICSetStatusProc
title: ICSetStatusProc function
author: windows-sdk-content
description: The ICSetStatusProc function sends the address of a status callback function to a compressor. The compressor calls this function during lengthy operations.
old-location: multimedia\icsetstatusproc.htm
tech.root: Multimedia
ms.assetid: 1e59a5ae-ac59-45fd-b80a-1908f1bf0d5e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ICSetStatusProc, ICSetStatusProc function [Windows Multimedia], _win32_ICSetStatusProc, multimedia.icsetstatusproc, vfw/ICSetStatusProc
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICSetStatusProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICSetStatusProc function


## -description



The <b>ICSetStatusProc</b> function sends the address of a status callback function to a compressor. The compressor calls this function during lengthy operations.




## -parameters




### -param hic

Handle to the compressor.


### -param dwFlags

Applicable flags. Set to zero.


### -param lParam

Constant specified with the status callback address.


### -param fpfnStatus

Pointer to the status callback function. Specify <b>NULL</b> to indicate no status callbacks should be sent.


## -returns



Returns ICERR_OK if successful or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

