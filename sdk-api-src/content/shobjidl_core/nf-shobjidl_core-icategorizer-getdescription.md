---
UID: NF:shobjidl_core.ICategorizer.GetDescription
title: ICategorizer::GetDescription (shobjidl_core.h)
description: Gets the name of a categorizer, such as Group By Device Type, that can be displayed in the UI.
helpviewer_keywords: ["GetDescription","GetDescription method [Windows Shell]","GetDescription method [Windows Shell]","ICategorizer interface","ICategorizer interface [Windows Shell]","GetDescription method","ICategorizer.GetDescription","ICategorizer::GetDescription","inet_ICategorizer_GetDescription","shell.ICategorizer_GetDescription","shobjidl_core/ICategorizer::GetDescription"]
old-location: shell\ICategorizer_GetDescription.htm
tech.root: shell
ms.assetid: fc457b03-ccc2-4455-9f53-77d47537c0b6
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [Windows Shell], GetDescription method [Windows Shell],ICategorizer interface, ICategorizer interface [Windows Shell],GetDescription method, ICategorizer.GetDescription, ICategorizer::GetDescription, inet_ICategorizer_GetDescription, shell.ICategorizer_GetDescription, shobjidl_core/ICategorizer::GetDescription
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICategorizer::GetDescription
 - shobjidl_core/ICategorizer::GetDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICategorizer.GetDescription
---

# ICategorizer::GetDescription


## -description

Gets the name of a categorizer, such as <i>Group By Device Type</i>, that can be displayed in the UI.

## -parameters

### -param pszDesc [out]

Type: <b>LPWSTR</b>

When this method returns, contains a pointer to a string of length <i>cch</i> that contains the categorizer name.

### -param cch [in]

Type: <b>UINT</b>

The number of characters in the <i>pszDesc</i> buffer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In the case of the system folder view object, if the description at <i>pszDesc</i> matches one of the category names listed in the folder's <b>Arrange Icons By</b> menu, a dot is placed by that name when the menu is displayed, either through the <b>View</b> menu or through the context menu.

