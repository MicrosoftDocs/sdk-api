---
UID: NF:shobjidl_core.SHCreateShellItemArrayFromDataObject
title: SHCreateShellItemArrayFromDataObject function
author: windows-sdk-content
description: Creates a Shell item array object from a data object.
old-location: shell\SHCreateShellItemArrayFromDataObject.htm
tech.root: shell
ms.assetid: 91e65c9a-0600-42e3-97f5-2a5960e1ec89
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: SHCreateShellItemArrayFromDataObject, SHCreateShellItemArrayFromDataObject function [Windows Shell], _shell_SHCreateShellItemArrayFromDataObject, shell.SHCreateShellItemArrayFromDataObject, shobjidl_core/SHCreateShellItemArrayFromDataObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreateShellItemArrayFromDataObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHCreateShellItemArrayFromDataObject function


## -description


Creates a Shell item array object from a data object. 


## -parameters




### -param pdo [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired interface ID.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is usefull for Shell extensions that implement <a href="https://msdn.microsoft.com/5f7e7f71-4cd6-4ce4-946c-9a1f7ec72fbe">IShellExtInit</a> and are passed a data object to the <a href="https://msdn.microsoft.com/1997a32e-562a-4d20-ad09-c40446a8feed">IShellExtInit::Initialize</a> method; for example, context menu handlers.

This API lets you convert the data object into a Shell item that the handler can consume. It is recommend that handlers use a Shell item array rather than clipboard formats like <b>CF_HDROP</b> and <b>CFSTR_SHELLIDLIST</b> (also known as HIDA) as it leads to simpler code and allows some performance improvements.

The resulting shell item array holds a reference to the source data object.  Therefore, that data object must remain valid for the lifetime of the shell item array.  Notably, the data objects passed to <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> methods are no longer valid after the drop operation completes.



