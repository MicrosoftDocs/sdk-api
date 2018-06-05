---
UID: NF:shobjidl_core.SHCreateItemFromRelativeName
title: SHCreateItemFromRelativeName function
author: windows-sdk-content
description: Creates and initializes a Shell item object from a relative parsing name.
old-location: shell\SHCreateItemFromRelativeName.htm
old-project: shell
ms.assetid: af6c2e8b-c812-4858-a9db-24549dedc2aa
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHCreateItemFromRelativeName, SHCreateItemFromRelativeName function [Windows Shell], _shell_SHCreateItemFromRelativeName, shell.SHCreateItemFromRelativeName, shobjidl_core/SHCreateItemFromRelativeName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	SHCreateItemFromRelativeName
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SHCreateItemFromRelativeName function


## -description


Creates and initializes a Shell item object from a relative parsing name.


## -parameters




### -param psiParent [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the parent Shell item.


### -param pszName [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated, Unicode string that specifies a display name that is relative to the <i>psiParent</i>.


### -param pbc [in]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to a bind context that controls the parsing operation. This parameter can be <b>NULL</b>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to an interface ID.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in riid.  This will usually be <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or 
        <a href="https://msdn.microsoft.com/e54d8385-ec67-4825-ad7c-431807a4fcb4">IShellItem2</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



