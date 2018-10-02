---
UID: NF:shobjidl_core.SHGetPropertyStoreFromParsingName
title: SHGetPropertyStoreFromParsingName function
author: windows-sdk-content
description: Returns a property store for an item, given a path or parsing name.
old-location: properties\SHGetPropertyStoreFromParsingName.htm
tech.root: properties
ms.assetid: 0d8d2e70-8200-4153-bd52-f7d839fd0909
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: SHGetPropertyStoreFromParsingName, SHGetPropertyStoreFromParsingName function [Windows Properties], _shell_SHGetPropertyStoreFromParsingName, properties.SHGetPropertyStoreFromParsingName, shell.SHGetPropertyStoreFromParsingName, shobjidl_core/SHGetPropertyStoreFromParsingName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shobjidl_core.h
req.include-header: 
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetPropertyStoreFromParsingName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHGetPropertyStoreFromParsingName function


## -description


Returns a property store for an item, given a path or parsing name.


## -parameters




### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the item path.


### -param pbc [in, optional]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> object, which provides access to a bind context. This value can be <b>NULL</b>.


### -param flags [in]

Type: <b><a href="shell.GETPROPERTYSTOREFLAGS">GETPROPERTYSTOREFLAGS</a></b>

One or more values from the <a href="shell.GETPROPERTYSTOREFLAGS">GETPROPERTYSTOREFLAGS</a> constants. This parameter can also be <b>NULL</b>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired interface ID.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="shell.IPropertyStore">IPropertyStore</a> or a related interface.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a>
 

 

