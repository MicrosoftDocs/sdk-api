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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQueryAssociations::GetData


## -description


Searches for and retrieves file or protocol association-related binary data from the registry.


## -parameters




### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF</a></b>

The <a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF</a> value that can be used to control the search.


### -param data [in]

Type: <b><a href="https://msdn.microsoft.com/0ae5c8db-81fd-4d00-8e54-0c474f1bfd06">ASSOCDATA</a></b>

The <a href="https://msdn.microsoft.com/0ae5c8db-81fd-4d00-8e54-0c474f1bfd06">ASSOCDATA</a> value that specifies the type of data that is to be returned.


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




<a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a>
 

 

