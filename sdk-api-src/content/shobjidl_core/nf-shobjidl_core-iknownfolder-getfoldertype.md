---
UID: NF:shobjidl_core.IKnownFolder.GetFolderType
title: IKnownFolder::GetFolderType
author: windows-sdk-content
description: Retrieves the folder type.
old-location: shell\IKnownFolder_GetFolderType.htm
tech.root: shell
ms.assetid: a2457d52-390d-43bd-8db0-9c18492cc40e
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetFolderType, GetFolderType method [Windows Shell], GetFolderType method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetFolderType method, IKnownFolder.GetFolderType, IKnownFolder::GetFolderType, _shell_IKnownFolder_GetFolderType, shell.IKnownFolder_GetFolderType, shobjidl_core/IKnownFolder::GetFolderType
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IKnownFolder.GetFolderType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolder::GetFolderType


## -description


Retrieves the folder type.


## -parameters




### -param pftid [out]

Type: <b><a href="https://msdn.microsoft.com/d147a05c-6a03-4f20-a7be-20825fcbeec2">FOLDERTYPEID</a>*</b>

When this returns, contains a pointer to a <a href="https://msdn.microsoft.com/d147a05c-6a03-4f20-a7be-20825fcbeec2">FOLDERTYPEID</a> (a GUID) that identifies the known folder type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

