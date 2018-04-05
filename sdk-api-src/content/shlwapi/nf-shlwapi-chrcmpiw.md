---
UID: NF:shlwapi.ChrCmpIW
title: ChrCmpIW function
author: windows-driver-content
description: Performs a comparison between two characters. The comparison is not case-sensitive.
old-location: shell\ChrCmpI.htm
old-project: shell
ms.assetid: ae2f3cbf-c65b-41a4-8d59-39d6fadf40ca
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ChrCmpI, ChrCmpI function [Windows Shell], ChrCmpIA, ChrCmpIW, _win32_ChrCmpI, shell.ChrCmpI, shlwapi/ChrCmpI, shlwapi/ChrCmpIA, shlwapi/ChrCmpIW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
api_name:
-	ChrCmpI
-	ChrCmpIA
-	ChrCmpIW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
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



