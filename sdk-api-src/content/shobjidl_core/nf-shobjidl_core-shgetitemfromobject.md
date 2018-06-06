---
UID: NF:shobjidl_core.SHGetItemFromObject
title: SHGetItemFromObject function
author: windows-sdk-content
description: Retrieves an IShellItem for an object.
old-location: shell\SHGetItemFromObject.htm
old-project: shell
ms.assetid: 0ef494c0-81c7-4fbd-9c37-78861d8ac63b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHGetItemFromObject, SHGetItemFromObject function [Windows Shell], _shell_SHGetItemFromObject, shell.SHGetItemFromObject, shobjidl_core/SHGetItemFromObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
api_name:
 - SHGetItemFromObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SHGetItemFromObject function


## -description


Retrieves an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> for an object.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the object.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired IID.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or a related interface.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



From the standpoint of performance, this method is preferred to <a href="https://msdn.microsoft.com/42821075-8123-4bfa-a6ba-8d3a77a9f50b">SHGetIDListFromObject</a> in those cases where the IDList is already bound to a folder.




## -see-also




<a href="https://msdn.microsoft.com/a6dcddd9-cdbc-4cf9-97e3-d1b562283344">SHCreateItemFromIDList</a>



<a href="https://msdn.microsoft.com/42821075-8123-4bfa-a6ba-8d3a77a9f50b">SHGetIDListFromObject</a>
 

 

