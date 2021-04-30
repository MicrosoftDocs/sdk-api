---
UID: NF:shobjidl_core.ICategoryProvider.GetCategoryForSCID
title: ICategoryProvider::GetCategoryForSCID (shobjidl_core.h)
description: Gets a GUID that represents the categorizer to use for the specified Shell column.
helpviewer_keywords: ["GetCategoryForSCID","GetCategoryForSCID method [Windows Shell]","GetCategoryForSCID method [Windows Shell]","ICategoryProvider interface","ICategoryProvider interface [Windows Shell]","GetCategoryForSCID method","ICategoryProvider.GetCategoryForSCID","ICategoryProvider::GetCategoryForSCID","inet_ICategoryProvider_GetCategoryForSCID","shell.ICategoryProvider_GetCategoryForSCID","shobjidl_core/ICategoryProvider::GetCategoryForSCID"]
old-location: shell\ICategoryProvider_GetCategoryForSCID.htm
tech.root: shell
ms.assetid: 52b4fac7-14bd-4d58-a00d-f102e013df16
ms.date: 12/05/2018
ms.keywords: GetCategoryForSCID, GetCategoryForSCID method [Windows Shell], GetCategoryForSCID method [Windows Shell],ICategoryProvider interface, ICategoryProvider interface [Windows Shell],GetCategoryForSCID method, ICategoryProvider.GetCategoryForSCID, ICategoryProvider::GetCategoryForSCID, inet_ICategoryProvider_GetCategoryForSCID, shell.ICategoryProvider_GetCategoryForSCID, shobjidl_core/ICategoryProvider::GetCategoryForSCID
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
 - ICategoryProvider::GetCategoryForSCID
 - shobjidl_core/ICategoryProvider::GetCategoryForSCID
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
 - ICategoryProvider.GetCategoryForSCID
---

# ICategoryProvider::GetCategoryForSCID


## -description

Gets a GUID that represents the categorizer to use for the specified Shell column.

## -parameters

### -param pscid [in]

Type: <b>const <a href="/windows/desktop/shell/objects">SHCOLUMNID</a>*</b>

A pointer to a <a href="/windows/desktop/shell/objects">SHCOLUMNID</a> structure.

### -param pguid [out]

Type: <b>GUID*</b>

When this method returns, contains a pointer to a GUID that represents the categorizer to use for the <a href="/windows/desktop/shell/objects">SHCOLUMNID</a> pointed to by <i>pscid</i>.

## -returns

Type: <b>HRESULT</b>

Returns either S_OK on success or S_FALSE on failure.