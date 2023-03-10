---
UID: NF:shimgdata.IShellImageData.GetCurrentPage
title: IShellImageData::GetCurrentPage (shimgdata.h)
description: Gets the current page of a multipage image.
helpviewer_keywords: ["GetCurrentPage","GetCurrentPage method [Windows Shell]","GetCurrentPage method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","GetCurrentPage method","IShellImageData.GetCurrentPage","IShellImageData::GetCurrentPage","_shell_IShellImageData_GetCurrentPage","shell.IShellImageData_GetCurrentPage","shimgdata/IShellImageData::GetCurrentPage"]
old-location: shell\IShellImageData_GetCurrentPage.htm
tech.root: shell
ms.assetid: 75489f7f-1ec5-471c-bc45-c8f480b0fa99
ms.date: 12/05/2018
ms.keywords: GetCurrentPage, GetCurrentPage method [Windows Shell], GetCurrentPage method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetCurrentPage method, IShellImageData.GetCurrentPage, IShellImageData::GetCurrentPage, _shell_IShellImageData_GetCurrentPage, shell.IShellImageData_GetCurrentPage, shimgdata/IShellImageData::GetCurrentPage
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
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
 - IShellImageData::GetCurrentPage
 - shimgdata/IShellImageData::GetCurrentPage
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
 - IShellImageData.GetCurrentPage
---

# IShellImageData::GetCurrentPage


## -description

Gets the current page of a multipage image.

## -parameters

### -param pnPage [out]

Type: <b>ULONG*</b>

A pointer to the page number.

## -returns

Type: <b>HRESULT</b>

Returns S_OK. If the image is not a multipage image, such as a .jpg file, the method returns S_OK with a page number of 0.

