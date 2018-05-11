---
UID: NF:shlobj_core.SHGetRealIDL
title: SHGetRealIDL function
author: windows-driver-content
description: SHGetRealIDL may be altered or unavailable.
old-location: shell\SHGetRealIDL.htm
old-project: shell
ms.assetid: 0c0b63c9-7ca7-4f73-be74-9c492f8506fc
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SHGetRealIDL, SHGetRealIDL function [Windows Shell], _win32_SHGetRealIDL, shell.SHGetRealIDL, shlobj_core/SHGetRealIDL
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
-	SHGetRealIDL
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHGetRealIDL function


## -description


<p class="CCE_Message">[<b>SHGetRealIDL</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Converts a simple pointer to an item identifier list (PIDL) into a full PIDL.


## -parameters




### -param psf [in]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to an instance of <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> whose simple PIDL is to be converted.


### -param pidlSimple [in]

Type: <b>PCUITEMID_CHILD</b>

The simple PIDL to be converted.


### -param ppidlReal [out]

Type: <b>PITEMID_CHILD*</b>

When this method returns, contains a pointer to the full converted PIDL. If the function fails, this parameter is set to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



