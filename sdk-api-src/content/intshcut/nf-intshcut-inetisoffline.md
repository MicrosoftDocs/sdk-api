---
UID: NF:intshcut.InetIsOffline
title: InetIsOffline function (intshcut.h)
description: Determines whether the system is connected to the Internet.
helpviewer_keywords: ["InetIsOffline","InetIsOffline function [Windows Shell]","_win32_InetIsOffline","intshcut/InetIsOffline","shell.InetIsOffline"]
old-location: shell\InetIsOffline.htm
tech.root: shell
ms.assetid: e0afac1c-c083-4b60-a30f-5dfc1a4b8fd3
ms.date: 12/05/2018
ms.keywords: InetIsOffline, InetIsOffline function [Windows Shell], _win32_InetIsOffline, intshcut/InetIsOffline, shell.InetIsOffline
req.header: intshcut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Url.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InetIsOffline
 - intshcut/InetIsOffline
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Url.dll
api_name:
 - InetIsOffline
---

# InetIsOffline function


## -description

Determines whether the system is connected to the Internet.

## -parameters

### -param dwFlags

Type: <b>DWORD</b>

The input flags for the function. This must be set to zero.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the local system is not currently connected to the Internet. Returns <b>FALSE</b> if the local system is connected to the Internet or if no attempt has yet been made to connect to the Internet.

