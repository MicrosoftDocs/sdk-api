---
UID: NF:shobjidl_core.IKnownFolder.GetId
title: IKnownFolder::GetId
author: windows-sdk-content
description: Gets the ID of the selected folder.
old-location: shell\IKnownFolder_GetId.htm
tech.root: shell
ms.assetid: c20fc32f-394d-4fbe-b7dd-072d84be2713
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetId, GetId method [Windows Shell], GetId method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetId method, IKnownFolder.GetId, IKnownFolder::GetId, _shell_IKnownFolder_GetId, shell.IKnownFolder_GetId, shobjidl_core/IKnownFolder::GetId
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
 - IKnownFolder.GetId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolder::GetId


## -description


Gets the ID of the selected folder.


## -parameters




### -param pkfid [out]

Type: <b><a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>*</b>

When this method returns, returns the <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> value of the known folder. Note, <b>KNOWNFOLDERID</b> values are GUIDs.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

