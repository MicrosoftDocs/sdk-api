---
UID: NF:winternl.RtlInitString
title: RtlInitString function (winternl.h)
description: Initializes a counted string.
helpviewer_keywords: ["RtlInitString","RtlInitString function [Windows API]","winprog.rtlinitstring","winternl/RtlInitString","winui.rtlinitstring"]
old-location: winprog\rtlinitstring.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlinitstring.htm
ms.date: 12/05/2018
ms.keywords: RtlInitString, RtlInitString function [Windows API], winprog.rtlinitstring, winternl/RtlInitString, winui.rtlinitstring
req.header: winternl.h
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
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlInitString
 - winternl/RtlInitString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlInitString
---

# RtlInitString function


## -description

Initializes a counted string.

## -parameters

### -param DestinationString [in, out]

The counted string to be initialized. The <i>DestinationString</i> is initialized to point to the <i>SourceString</i>. The <b>Length</b> and <b>MaximumLength</b> fields of the <i>DestinationString</i> are initialized to the length of the <i>SourceString</i>.

### -param SourceString [in]

A pointer to a null-terminated string. If the <i>SourceString</i> is not specified, the <b>Length</b> and <b>MaximumLength</b> fields of the <i>DestinationString</i> are initialized to zero.

## -remarks

<b>Security Warning:  </b>Do not allow the <i>SourceString</i> parameter size to exceed <b>MAX_USHORT</b> characters.

Because there is no import library for this function, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.


		

<div class="alert"><b>Note</b>  <b>RtlInitString</b> is available in Windows XP. It might be altered or unavailable in subsequent versions.</div>
<div> </div>