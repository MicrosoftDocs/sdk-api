---
UID: NF:shobjidl_core.SHGetPropertyStoreFromParsingName
title: SHGetPropertyStoreFromParsingName function (shobjidl_core.h)
author: windows-sdk-content
description: Returns a property store for an item, given a path or parsing name.
old-location: properties\SHGetPropertyStoreFromParsingName.htm
tech.root: properties
ms.assetid: 0d8d2e70-8200-4153-bd52-f7d839fd0909
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SHGetPropertyStoreFromParsingName, SHGetPropertyStoreFromParsingName function [Windows Properties], _shell_SHGetPropertyStoreFromParsingName, properties.SHGetPropertyStoreFromParsingName, shell.SHGetPropertyStoreFromParsingName, shobjidl_core/SHGetPropertyStoreFromParsingName
ms.topic: function
f1_keywords: ["shobjidl_core/SHGetPropertyStoreFromParsingName"]
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
ms.custom: 19H1
---

# SHGetPropertyStoreFromParsingName function


## -description


Returns a property store for an item, given a path or parsing name.


## -parameters




### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the item path.


### -param pbc [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> object, which provides access to a bind context. This value can be <b>NULL</b>.


### -param flags [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a></b>

One or more values from the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags">GETPROPERTYSTOREFLAGS</a> constants. This parameter can also be <b>NULL</b>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired interface ID.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> or a related interface.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a>
 

 

