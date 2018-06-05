---
UID: NF:winternl.RtlFreeAnsiString
title: RtlFreeAnsiString function
author: windows-sdk-content
description: Frees the string buffer allocated by RtlUnicodeStringToAnsiString.
old-location: winprog\rtlfreeansistring.htm
old-project: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlfreeansistring.htm
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: RtlFreeAnsiString, RtlFreeAnsiString function [Windows API], winprog.rtlfreeansistring, winternl/RtlFreeAnsiString, winui.rtlfreeansistring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
tech.root: 
req.typenames: SYNC_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdll.dll
api_name:
-	RtlFreeAnsiString
product: Windows
targetos: Windows
req.lib: 
req.dll: Ntdll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RtlFreeAnsiString function


## -description


Frees the string buffer allocated by <a href="https://msdn.microsoft.com/library/windows/hardware/ff562969">RtlUnicodeStringToAnsiString</a>.


## -parameters




### -param AnsiString [in]

A pointer to an ANSI string whose buffer was previously allocated by <a href="https://msdn.microsoft.com/library/windows/hardware/ff562969">RtlUnicodeStringToAnsiString</a>.


## -returns



This function does not return a value.




## -remarks



This routine does not release the Unicode string buffer passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff562969">RtlUnicodeStringToAnsiString</a>.



