---
UID: NF:winternl.RtlFreeOemString
title: RtlFreeOemString function
author: windows-driver-content
description: Frees the string buffer allocated by RtlUnicodeStringToOemString.
old-location: winprog\rtlfreeoemstring.htm
old-project: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlfreeoemstring.htm
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: RtlFreeOemString, RtlFreeOemString function [Windows API], winprog.rtlfreeoemstring, winternl/RtlFreeOemString, winui.rtlfreeoemstring
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SYNC_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdll.dll
api_name:
-	RtlFreeOemString
product: Windows
targetos: Windows
req.lib: 
req.dll: Ntdll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RtlFreeOemString function


## -description


Frees the string buffer allocated by
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff553255">RtlUnicodeStringToOemString</a>.


## -parameters




### -param OemString [in, out]

Address of the OEM string whose buffer
        was previously allocated by <a href="https://msdn.microsoft.com/library/windows/hardware/ff553255">RtlUnicodeStringToOemString</a>.


## -returns



This function does not return a value.




## -remarks



This routine releases the <b>Buffer</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff558741">OEM_STRING</a> structure. The <b>Length</b> and <b>MaximumLength</b> members are not affected by this routine.
		



