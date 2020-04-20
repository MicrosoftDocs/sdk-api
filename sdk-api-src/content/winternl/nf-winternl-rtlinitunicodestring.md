---
UID: NF:winternl.RtlInitUnicodeString
title: RtlInitUnicodeString function (winternl.h)
description: Initializes a counted Unicode string.helpviewer_keywords: ["RtlInitUnicodeString","RtlInitUnicodeString function [Windows API]","winprog.rtlinitunicodestring","winternl/RtlInitUnicodeString","winui.rtlinitunicodestring"]
old-location: winprog\rtlinitunicodestring.htm
tech.root: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlinitunicodestring.htm
ms.date: 12/05/2018
ms.keywords: RtlInitUnicodeString, RtlInitUnicodeString function [Windows API], winprog.rtlinitunicodestring, winternl/RtlInitUnicodeString, winui.rtlinitunicodestring
f1_keywords:
- winternl/RtlInitUnicodeString
dev_langs:
- c++
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
req.lib: NtosKrnl.lib
req.dll: Ntdll.dll; NtosKrnl.exe
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ntdll.dll
- NtosKrnl.exe
api_name:
- RtlInitUnicodeString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtlInitUnicodeString function


## -description


Initializes a counted Unicode string.  


## -parameters




### -param DestinationString [in, out]

The buffer for a counted Unicode string to be initialized. The length is initialized to zero if the <i>SourceString</i> is not specified. 


### -param SourceString [in, optional]

Optional pointer to a null-terminated Unicode string with
        which to initialize the counted string. 


