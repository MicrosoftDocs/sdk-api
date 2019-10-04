---
UID: NF:shlwapi.IQueryAssociations.GetData
title: IQueryAssociations::GetData (shlwapi.h)
author: windows-sdk-content
description: Searches for and retrieves file or protocol association-related binary data from the registry.
old-location: shell\IQueryAssociations_GetData.htm
tech.root: shell
ms.assetid: 7f21e564-97c6-4f9d-a4fa-160b78dbfc2f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Windows Shell], GetData method [Windows Shell],IQueryAssociations interface, IQueryAssociations interface [Windows Shell],GetData method, IQueryAssociations.GetData, IQueryAssociations::GetData, _win32_IQueryAssociations_GetData, shell.IQueryAssociations_GetData, shlwapi/IQueryAssociations::GetData
ms.topic: method
f1_keywords: 
 - "shlwapi/IQueryAssociations.GetData"
dev_langs:
 - c++
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IQueryAssociations.GetData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IQueryAssociations::GetData


## -description


Searches for and retrieves file or protocol association-related binary data from the registry.


## -parameters




### -param flags [in]

Type: <b><a href="https://docs.microsoft.com/windows/win32/api/shlwapi/ne-shlwapi-url_scheme">ASSOCF</a></b>

The <a href="https://docs.microsoft.com/windows/win32/api/shlwapi/ne-shlwapi-url_scheme">ASSOCF</a> value that can be used to control the search.


### -param data [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/ne-shlwapi-assocdata">ASSOCDATA</a></b>

The <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/ne-shlwapi-assocdata">ASSOCDATA</a> value that specifies the type of data that is to be returned.


### -param pszExtra [in, optional]

Type: <b>LPCWSTR</b>

A pointer to an optional, null-terminated Unicode string with information about the location of the data. It is normally set to a Shell verb such as <b>open</b>. Set this parameter to <b>NULL</b> if it is not used.


### -param pvOut [out, optional]

Type: <b>void*</b>

A pointer to a value that, when this method returns successfully, receives the requested data value.


### -param pcbOut [in, out, optional]

Type: <b>DWORD*</b>

A pointer to a value that, when this method is called, holds the size of <i>pvOut</i>, in bytes. When this method returns successfully, the value contains the size of the data actually retrieved.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a>
 

 

