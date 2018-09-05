---
UID: NF:shobjidl_core.SHGetIDListFromObject
title: SHGetIDListFromObject function
author: windows-sdk-content
description: Retrieves the pointer to an item identifier list (PIDL) of an object.
old-location: shell\SHGetIDListFromObject.htm
old-project: shell
ms.assetid: 42821075-8123-4bfa-a6ba-8d3a77a9f50b
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SHGetIDListFromObject, SHGetIDListFromObject function [Windows Shell], _shell_SHGetIDListFromObject, shell.SHGetIDListFromObject, shobjidl_core/SHGetIDListFromObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - SHGetIDListFromObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SHGetIDListFromObject function


## -description


Retrieves the pointer to an item identifier list (PIDL) of an object.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the object from which to get the PIDL.


### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this function returns, contains a pointer to the PIDL of the given object.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a6dcddd9-cdbc-4cf9-97e3-d1b562283344">SHCreateItemFromIDList</a>
 

 

