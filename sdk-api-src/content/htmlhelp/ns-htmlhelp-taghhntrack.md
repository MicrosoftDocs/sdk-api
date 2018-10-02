---
UID: NS:htmlhelp.tagHHNTRACK
title: tagHHNTRACK
author: windows-sdk-content
description: This structure returns the file name of the current topic and a constant that specifies the user action that is about to occur, such as hiding the Navigation pane by clicking the Hide button on the toolbar.
old-location: htmlhelp\hhntrack_structure.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\vsconstrhhntrack.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: HHNTRACK, HHNTRACK structure [HTML Help Workshop], htmlhelp.hhntrack_structure, htmlhelp/HHNTRACK, tagHHNTRACK, vsconStrhhntrack
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: htmlhelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - HtmlHelp.h
api_name:
 - HHNTRACK
product: Windows
targetos: Windows
req.typenames: HHNTRACK
req.redist: 
---

# tagHHNTRACK structure


## -description


This structure returns the file name of the current topic and a constant that specifies the user action that is about to occur, such as hiding the Navigation pane by clicking the Hide button on the toolbar. 


## -struct-fields




### -field hdr

Standard <b>WM_NOTIFY</b> header. 


### -field pszCurUrl

A multi-byte, zero-terminated string that specifies the current topic (before the action is taken). 


### -field idAction

Specifies the action the user is about to take. This is an <a href="https://msdn.microsoft.com/E09BFFD7-8E44-47ba-BAFD-4582FF9430A7">HHACT_</a> constant. 


### -field phhWinType

A pointer to the current <a href="https://msdn.microsoft.com/61614318-9785-4f1e-A9E7-366C04DE4FFE">HH_WINTYPE</a> structure. 


## -see-also




<a href="https://msdn.microsoft.com/E75CA82E-9759-47d8-AF84-5842EDAB019D">About structures</a>
 

 

