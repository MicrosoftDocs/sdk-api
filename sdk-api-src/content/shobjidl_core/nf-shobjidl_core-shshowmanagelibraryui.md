---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SHShowManageLibraryUI function


## -description


Shows the library management dialog box, which enables users to manage the library folders and default save location.


## -parameters




### -param psiLibrary [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object that represents the library that is to be managed.


### -param hwndOwner [in, optional]

Type: <b>HWND</b>

The handle for the window that owns the library management dialog box. The value of this parameter can be <b>NULL</b>.


### -param pszTitle [in, optional]

Type: <b>LPCWSTR</b>

A pointer to the title for the library management dialog. To display the generic title string, set the value of this parameter to <b>NULL</b>.


### -param pszInstruction [in, optional]

Type: <b>LPCWSTR</b>

A pointer to a help string to display below the title string in the library management dialog box. To display the generic help string, set the value of this parameter to <b>NULL</b>.


### -param lmdOptions [in]

Type: <b><a href="https://msdn.microsoft.com/e5eaf131-9562-4ab0-a8bc-4eaaaa806a8f">LIBRARYMANAGEDIALOGOPTIONS</a></b>

A value from the <a href="https://msdn.microsoft.com/e5eaf131-9562-4ab0-a8bc-4eaaaa806a8f">LIBRARYMANAGEDIALOGOPTIONS</a> enumeration that specifies the behavior of the management dialog box.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/e5eaf131-9562-4ab0-a8bc-4eaaaa806a8f">LIBRARYMANAGEDIALOGOPTIONS</a>
 

 

