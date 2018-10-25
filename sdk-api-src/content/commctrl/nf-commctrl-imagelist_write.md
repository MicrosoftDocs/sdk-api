---
UID: NF:commctrl.ImageList_Write
title: ImageList_Write function
author: windows-sdk-content
description: Writes an image list to a stream.
old-location: controls\ImageList_Write.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_write.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ImageList_Write, ImageList_Write function [Windows Controls], _win32_ImageList_Write, _win32_ImageList_Write_cpp, commctrl/ImageList_Write, controls.ImageList_Write, controls._win32_ImageList_Write
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_Write
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_Write function


## -description


Writes an image list to a stream. 


## -parameters




### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param pstm

Type: <b>LPSTREAM</b>

A pointer to the stream. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 



