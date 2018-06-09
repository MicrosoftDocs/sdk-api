---
UID: NS:tlogstg._WINDOWDATA
title: "_WINDOWDATA"
author: windows-sdk-content
description: Stores window data.
old-location: shell\WINDOWDATA.htm
old-project: shell
ms.assetid: ef83bd02-cde9-41a8-b5ad-a26794663ac2
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: "*LPWINDOWDATA, WINDOWDATA, WINDOWDATA structure [Windows Shell], _WINDOWDATA, _shell_WINDOWDATA, shell.WINDOWDATA, tlogstg/WINDOWDATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tlogstg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tlogstg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WINDOWDATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tlogstg.h
api_name:
 - WINDOWDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _WINDOWDATA structure


## -description


Stores window data.


## -struct-fields




### -field dwWindowID

Type: <b>DWORD</b>

The window ID.


### -field uiCP

Type: <b>UINT</b>

The codepage of the current entry.


### -field pidl

Type: <b>PIDLIST_ABSOLUTE</b>

The current PIDL.


### -field lpszUrl

Type: <b>LPWSTR</b>

A pointer to a buffer to hold the window URL.


### -field lpszUrlLocation

Type: <b>LPWSTR</b>

A pointer to a buffer to hold the window URL Location (local anchor).


### -field lpszTitle

Type: <b>LPWSTR</b>

A pointer to a buffer to hold the window title.

