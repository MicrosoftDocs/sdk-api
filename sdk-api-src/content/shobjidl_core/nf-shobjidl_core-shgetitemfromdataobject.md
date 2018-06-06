---
UID: NF:shobjidl_core.SHGetItemFromDataObject
title: SHGetItemFromDataObject function
author: windows-sdk-content
description: Creates an IShellItem or related object based on an item specified by an IDataObject.
old-location: shell\SHGetItemFromDataObject.htm
old-project: shell
ms.assetid: 1d7b9ffa-9980-4d68-85e4-7bab667be168
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHGetItemFromDataObject, SHGetItemFromDataObject function [Windows Shell], _shell_SHGetItemFromDataObject, shell.SHGetItemFromDataObject, shobjidl_core/SHGetItemFromDataObject
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
 - SHGetItemFromDataObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# SHGetItemFromDataObject function


## -description


Creates an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or related object based on an item specified by an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>.


## -parameters




### -param pdtobj [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to the source <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> instance.


### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/7a5ee490-cf30-452a-ade2-22d875ce0358">DATAOBJ_GET_ITEM_FLAGS</a></b>

One or more values from the <a href="https://msdn.microsoft.com/7a5ee490-cf30-452a-ade2-22d875ce0358">DATAOBJ_GET_ITEM_FLAGS</a> enumeration to specify options regarding the target object. This value can be 0.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IShellItem.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is recommended that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.



