---
UID: NF:shlwapi.IQueryAssociations.Init
title: IQueryAssociations::Init
author: windows-sdk-content
description: Initializes the IQueryAssociations interface and sets the root key to the appropriate ProgID.
old-location: shell\IQueryAssociations_Init.htm
tech.root: shell
ms.assetid: cb1bcfc1-dbaa-48f8-8547-408f6560753e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CLSID, Executable name, File name extension, IQueryAssociations interface [Windows Shell],Init method, IQueryAssociations.Init, IQueryAssociations::Init, Init, Init method [Windows Shell], Init method [Windows Shell],IQueryAssociations interface, ProgID, _win32_IQueryAssociations_Init, shell.IQueryAssociations_Init, shlwapi/IQueryAssociations::Init
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IQueryAssociations.Init
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQueryAssociations::Init


## -description


Initializes the <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> interface and sets the root key to the appropriate ProgID.


## -parameters




### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF</a></b>

A flag that specifies how the search is to be initialized. It is typically set to zero, but it can also take one of the following <a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF</a> values. 
					
                    

<ul>
<li>
<a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_INIT_BYEXENAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_INIT_DEFAULTTOFOLDER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_INIT_DEFAULTTOSTAR</a>
</li>
</ul>

### -param pszAssoc [in, optional]

Type: <b>LPCWSTR</b>

A Unicode string that is used to determine the root key. If a value is specified for <i>hkProgid</i>, set this parameter to <b>NULL</b>. Four types of string can be used:



#### File name extension

A file name extension, such as .txt.



#### CLSID

A CLSID GUID in the standard "{GUID}" format.



#### ProgID

An application's ProgID, such as <b>Word.Document.8</b>.



#### Executable name

The name of an application's .exe file. The <a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_OPEN_BYEXENAME</a> flag must be set in <i>flags</i>.


### -param hkProgid [in, optional]

Type: <b>HKEY</b>

The HKEY value of the subkey that is used as a root key. The search looks only below this key. If a value is specified for <i>pwszAssoc</i>, set this parameter to <b>NULL</b>.


### -param hwnd [in, optional]

Type: <b>HWND</b>


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method initializes the interface, and is also called each time you need to specify a new root key. You can use <i>pwszAssoc</i> to specify a string, such as a file name extension or its associated ProgID, that identifies the root key. You can also specify the root key's HKEY value. <b>Init</b> will then use this information to locate the root key in the registry. Subsequent calls to the other <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> methods will use it as their starting point and search for the information in the root key's subkeys.




## -see-also




<a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a>
 

 

