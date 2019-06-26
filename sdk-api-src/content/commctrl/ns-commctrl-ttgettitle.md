---
UID: NS:commctrl._TTGETTITLE
title: TTGETTITLE (commctrl.h)
author: windows-sdk-content
description: Provides information about the title of a tooltip control.
old-location: controls\TTGETTITLE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tooltip\structures\ttgettitle.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PTTGETTITLE, PTTGETTITLE, PTTGETTITLE structure pointer [Windows Controls], TTGETTITLE, TTGETTITLE structure [Windows Controls], commctrl/PTTGETTITLE, commctrl/TTGETTITLE, controls.TTGETTITLE, controls.inet_TTGETTITLE, inet_TTGETTITLE, inet_TTGETTITLE_cpp"
ms.topic: struct
f1_keywords: 
 - "commctrl/TTGETTITLE"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TTGETTITLE
product: Windows
targetos: Windows
req.typenames: TTGETTITLE, *PTTGETTITLE
req.redist: 
ms.custom: 19H1
---

# TTGETTITLE structure


## -description


Provides information about the title of a tooltip control.  



## -struct-fields




### -field dwSize

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

<b>DWORD</b> that specifies size of structure. Set to sizeof(TTGETTITLE).


### -field uTitleBitmap

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

<b>UINT</b> that specifies the tooltip icon.


### -field cch

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

<b>UINT</b> that specifies the number of characters in the title.


### -field pszTitle

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">WCHAR</a>*</b>

Pointer to a wide character string that contains the title.

