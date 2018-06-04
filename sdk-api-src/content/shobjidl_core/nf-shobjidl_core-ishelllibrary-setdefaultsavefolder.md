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

# IShellLibrary::SetDefaultSaveFolder


## -description


Sets the default target folder that the library will use for save operations.


## -parameters




### -param dsft [in]

Type: <b><a href="https://msdn.microsoft.com/51478854-03b2-4e1a-bc07-b9ca7e6cc33d">DEFAULTSAVEFOLDERTYPE</a></b>

The <a href="https://msdn.microsoft.com/51478854-03b2-4e1a-bc07-b9ca7e6cc33d">DEFAULTSAVEFOLDERTYPE</a>  value  that specifies the default save location to set.


### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

An  <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object that represents the folder that to use as the default save location. The folder that this object represents must be a folder that is already in the library.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The default save location must be valid, have read/write access, and with either the <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">SFGAO_STREAM</a> or <a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">SFGAO_FILESYSTEM</a> attribute set.

If <i>psi</i> is not in the library, this method returns an error.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/12F6E6AE-2776-408c-B9AC-E885BE93C27F">Library Description Schema</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

