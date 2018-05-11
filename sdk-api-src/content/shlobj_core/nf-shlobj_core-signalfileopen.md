---
UID: NF:shlobj_core.SignalFileOpen
title: SignalFileOpen function
author: windows-driver-content
description: SignalFileOpen may be altered or unavailable.
old-location: shell\SignalFileOpen.htm
old-project: shell
ms.assetid: b46bb06f-a183-4a39-89bd-457fa4fe728f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SignalFileOpen, SignalFileOpen function [Windows Shell], _win32_SignalFileOpen, shell.SignalFileOpen, shlobj_core/SignalFileOpen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	SignalFileOpen
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SignalFileOpen function


## -description


<p class="CCE_Message">[<b>SignalFileOpen</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sends a notification to the Shell that the specified file has been opened.


## -parameters




### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL that specifies the file.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise <b>FALSE</b>.



