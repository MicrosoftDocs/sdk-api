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

# SHCreateDefaultContextMenu function


## -description


Creates an object that represents the Shell's default context menu implementation.


## -parameters




### -param pdcm [in]

Type: <b>const <a href="https://msdn.microsoft.com/007861f6-1e66-4c5f-a459-3cfbe9f8cec2">DEFCONTEXTMENU</a>*</b>

A pointer to a constant <a href="https://msdn.microsoft.com/007861f6-1e66-4c5f-a459-3cfbe9f8cec2">DEFCONTEXTMENU</a> structure.


### -param riid

Type: <b>REFIID</b>

Reference to the interface ID of the interface on which to base the object. This is typically the IID of <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a>, <a href="https://msdn.microsoft.com/4e3331ad-4adc-4ea9-8a22-6aad15f618c8">IContextMenu2</a>, or <a href="https://msdn.microsoft.com/c08e1b98-2b8b-41f6-93c5-3a5937bd3b2c">IContextMenu3</a>.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is typically used in the implementation of <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a>. <b>GetUIObjectOf</b> creates a context menu that merges <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> handlers specified by the <a href="https://msdn.microsoft.com/007861f6-1e66-4c5f-a459-3cfbe9f8cec2">DEFCONTEXTMENU</a> structure, and can optionally provide default context menu verb implementations such as open, explore, delete, and copy.


             The operation of this function is controlled by the input specified in the <a href="https://msdn.microsoft.com/007861f6-1e66-4c5f-a459-3cfbe9f8cec2">DEFCONTEXTMENU</a> structure.The API<a href="https://msdn.microsoft.com/7b5e012d-1c8b-42c5-8181-9923fd389fc5">CDefFolderMenu_Create2</a> is another way to construct the default context menu implementation. It is less expressive than <b>SHCreateDefaultContextMenu</b> but it exists in platforms prior to Windows Vista.
           



