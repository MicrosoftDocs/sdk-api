---
UID: NF:shlwapi.AssocQueryKeyA
title: AssocQueryKeyA function
author: windows-sdk-content
description: Searches for and retrieves a key related to a file or protocol association from the registry.
old-location: shell\AssocQueryKey.htm
old-project: shell
ms.assetid: 9eaeb885-0428-48c3-82a7-5dc21d5015ce
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AssocQueryKey, AssocQueryKey function [Windows Shell], AssocQueryKeyA, AssocQueryKeyW, CLSID, Executable name, File name extension, ProgID, _win32_AssocQueryKey, shell.AssocQueryKey, shlwapi/AssocQueryKey, shlwapi/AssocQueryKeyA, shlwapi/AssocQueryKeyW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AssocQueryKeyW (Unicode) and AssocQueryKeyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
api_name:
 - AssocQueryKey
 - AssocQueryKeyA
 - AssocQueryKeyW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# AssocQueryKeyA function


## -description


Searches for and retrieves a key related to a file or protocol association from the registry.


## -parameters




### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF</a></b>

The flags that can be used to control the search. It can be any combination of <a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF</a> values, except that only one ASSOCF_INIT value can be included.


### -param key [in]

Type: <b><a href="https://msdn.microsoft.com/f4ac0ba0-4113-498f-a51b-74a37fe33d49">ASSOCKEY</a></b>

The <a href="https://msdn.microsoft.com/f4ac0ba0-4113-498f-a51b-74a37fe33d49">ASSOCKEY</a> value that specifies the type of key that is to be returned.


### -param pszAssoc [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that is used to determine the root key. Four types of strings can be used.



#### File name extension

A file name extension, such as .txt.



#### CLSID

A CLSID GUID in the standard "{GUID}" format.



#### ProgID

An application's ProgID, such as <b>Word.Document.8</b>.



#### Executable name

The name of an application's .exe file. The <a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_OPEN_BYEXENAME</a> flag must be set in <i>flags</i>.


### -param pszExtra [in]

Type: <b>LPCTSTR</b>

A pointer to an optional null-terminated string with additional information about the location of the string. It is normally set to a Shell verb such as <b>open</b>. Set this parameter to <b>NULL</b> if it is not used.


### -param phkeyOut [out]

Type: <b>HKEY*</b>

A pointer to the key's HKEY value.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



This function is a wrapper for the <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> interface. It is intended to simplify the process of using the interface. For further discussion of how the file and protocol association functions work, see <b>IQueryAssociations</b>.



