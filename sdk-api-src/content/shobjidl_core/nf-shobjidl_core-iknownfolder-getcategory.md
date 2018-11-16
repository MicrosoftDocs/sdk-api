---
UID: NF:shobjidl_core.IKnownFolder.GetCategory
title: IKnownFolder::GetCategory
author: windows-sdk-content
description: Retrieves the category&#8212;virtual, fixed, common, or per-user&#8212;of the selected folder.
old-location: shell\IKnownFolder_GetCategory.htm
tech.root: shell
ms.assetid: b3a7f249-9d57-4bd1-830f-1c83c745782f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetCategory, GetCategory method [Windows Shell], GetCategory method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetCategory method, IKnownFolder.GetCategory, IKnownFolder::GetCategory, _shell_IKnownFolder_GetCategory, shell.IKnownFolder_GetCategory, shobjidl_core/IKnownFolder::GetCategory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolder.GetCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IKnownFolder.GetCategory
: 
---

# IKnownFolder::GetCategory


## -description


Retrieves the category—virtual, fixed, common, or per-user—of the selected folder.


## -parameters




### -param pCategory [out]

Type: <b><a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">KF_CATEGORY</a>*</b>

When this method returns, contains a pointer to the <a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">KF_CATEGORY</a> of the selected folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

