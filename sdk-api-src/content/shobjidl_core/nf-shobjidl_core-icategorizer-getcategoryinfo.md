---
UID: NF:shobjidl_core.ICategorizer.GetCategoryInfo
title: ICategorizer::GetCategoryInfo (shobjidl_core.h)
author: windows-sdk-content
description: Gets information about a category, such as the default display and the text to display in the UI.
old-location: shell\ICategorizer_GetCategoryInfo.htm
tech.root: shell
ms.assetid: 6b789033-ce42-4fb5-8a3d-b05243b62d4e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCategoryInfo, GetCategoryInfo method [Windows Shell], GetCategoryInfo method [Windows Shell],ICategorizer interface, ICategorizer interface [Windows Shell],GetCategoryInfo method, ICategorizer.GetCategoryInfo, ICategorizer::GetCategoryInfo, inet_ICategorizer_GetCategoryInfo, shell.ICategorizer_GetCategoryInfo, shobjidl_core/ICategorizer::GetCategoryInfo
ms.topic: method
f1_keywords: ["shobjidl_core/ICategorizer.GetCategoryInfo"]
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICategorizer.GetCategoryInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICategorizer::GetCategoryInfo


## -description


Gets information about a category, such as the default display and the text to display in the UI.


## -parameters




### -param dwCategoryId [in]

Type: <b>DWORD</b>

A <b>DWORD</b> that specifies a category identifier.


### -param pci [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info">CATEGORY_INFO</a>*</b>

When this method returns, contains a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info">CATEGORY_INFO</a> structure that contains the category information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



