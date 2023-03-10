---
UID: NS:tlogstg._WINDOWDATA
title: WINDOWDATA (tlogstg.h)
description: Stores window data.
helpviewer_keywords: ["*LPWINDOWDATA","WINDOWDATA","WINDOWDATA structure [Windows Shell]","_shell_WINDOWDATA","shell.WINDOWDATA","tlogstg/WINDOWDATA"]
old-location: shell\WINDOWDATA.htm
tech.root: shell
ms.assetid: ef83bd02-cde9-41a8-b5ad-a26794663ac2
ms.date: 12/05/2018
ms.keywords: '*LPWINDOWDATA, WINDOWDATA, WINDOWDATA structure [Windows Shell], _shell_WINDOWDATA, shell.WINDOWDATA, tlogstg/WINDOWDATA'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WINDOWDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINDOWDATA
 - tlogstg/_WINDOWDATA
 - WINDOWDATA
 - tlogstg/WINDOWDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tlogstg.h
api_name:
 - WINDOWDATA
---

# WINDOWDATA structure


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

