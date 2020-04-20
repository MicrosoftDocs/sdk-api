---
UID: NF:shlwapi.ChrCmpIW
title: ChrCmpIW function (shlwapi.h)
description: Performs a comparison between two characters. The comparison is not case-sensitive.helpviewer_keywords: ["ChrCmpI","ChrCmpI function [Windows Shell]","ChrCmpIA","ChrCmpIW","_win32_ChrCmpI","shell.ChrCmpI","shlwapi/ChrCmpI","shlwapi/ChrCmpIA","shlwapi/ChrCmpIW"]
old-location: shell\ChrCmpI.htm
tech.root: shell
ms.assetid: ae2f3cbf-c65b-41a4-8d59-39d6fadf40ca
ms.date: 12/05/2018
ms.keywords: ChrCmpI, ChrCmpI function [Windows Shell], ChrCmpIA, ChrCmpIW, _win32_ChrCmpI, shell.ChrCmpI, shlwapi/ChrCmpI, shlwapi/ChrCmpIA, shlwapi/ChrCmpIW
f1_keywords:
- shlwapi/ChrCmpI
dev_langs:
- c++
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ChrCmpIW (Unicode) and ChrCmpIA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shlwapi.dll
api_name:
- ChrCmpI
- ChrCmpIA
- ChrCmpIW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ChrCmpIW function


## -description


Performs a comparison between two characters. The comparison is not case-sensitive.


## -parameters




### -param w1 [in]

Type: <b>TCHAR</b>

The first character to be compared.


### -param w2 [in]

Type: <b>TCHAR</b>

The second character to be compared.


## -returns



Type: <b>BOOL</b>

Returns zero if the two characters are the same, or nonzero otherwise.



