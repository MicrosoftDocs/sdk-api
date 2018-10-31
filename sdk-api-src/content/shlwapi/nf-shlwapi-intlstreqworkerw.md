---
UID: NF:shlwapi.IntlStrEqWorkerW
title: IntlStrEqWorkerW function
author: windows-sdk-content
description: Compares a specified number of characters from the beginning of two localized strings.
old-location: shell\IntlStrEqWorker.htm
tech.root: shell
ms.assetid: bc8e823e-79b2-49fd-950d-96a6e7256377
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IntlStrEqWorker, IntlStrEqWorker function [Windows Shell], IntlStrEqWorkerA, IntlStrEqWorkerW, _win32_IntlStrEqWorker, shell.IntlStrEqWorker, shlwapi/IntlStrEqWorker, shlwapi/IntlStrEqWorkerA, shlwapi/IntlStrEqWorkerW
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
req.unicode-ansi: IntlStrEqWorkerW (Unicode) and IntlStrEqWorkerA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - IntlStrEqWorker
 - IntlStrEqWorkerA
 - IntlStrEqWorkerW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IntlStrEqWorkerW function


## -description


Compares a specified number of characters from the beginning of two localized strings.


## -parameters




### -param fCaseSens [in]

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> for a case-sensitive comparison, or to <b>FALSE</b> for a case-insensitive comparison.


### -param lpString1 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string.


### -param lpString2 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string.


### -param nChar [in]

Type: <b>int</b>

The number of characters to be compared, starting from the beginning of the strings.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the first <i>nChar</i> characters are identical, or <b>FALSE</b> otherwise.




## -remarks



This function retrieves the thread locale and uses <a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a> to determine whether the first <i>nChar</i> characters are identical.



