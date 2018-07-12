---
UID: NF:commctrl.ImageList_EndDrag
title: ImageList_EndDrag function
author: windows-sdk-content
description: Ends a drag operation.
old-location: controls\ImageList_EndDrag.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_enddrag.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ImageList_EndDrag, ImageList_EndDrag function [Windows Controls], _win32_ImageList_EndDrag, _win32_ImageList_EndDrag_cpp, commctrl/ImageList_EndDrag, controls.ImageList_EndDrag, controls._win32_ImageList_EndDrag
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_EndDrag
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# ImageList_EndDrag function


## -description


Ends a drag operation. 


## -parameters






## -returns



None. 




## -remarks



The temporary image list is destroyed when the <b>ImageList_EndDrag</b> function is called. To begin a drag operation, use the <a href="https://msdn.microsoft.com/library/Bb761516(v=VS.85).aspx">ImageList_BeginDrag</a> function. 



