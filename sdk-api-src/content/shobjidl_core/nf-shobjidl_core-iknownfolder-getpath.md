---
UID: NF:shobjidl_core.IKnownFolder.GetPath
title: IKnownFolder::GetPath
author: windows-driver-content
description: Retrieves the path of a known folder as a string.
old-location: shell\IKnownFolder_GetPath.htm
old-project: shell
ms.assetid: c1786db0-9bcc-4fc8-ae18-8519da6edda9
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetPath, GetPath method [Windows Shell], GetPath method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetPath method, IKnownFolder.GetPath, IKnownFolder::GetPath, _shell_IKnownFolder_GetPath, shell.IKnownFolder_GetPath, shobjidl_core/IKnownFolder::GetPath
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IKnownFolder.GetPath
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IKnownFolder::GetPath


## -description


Retrieves the path of a known folder as a string.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify special retrieval options. This value can be 0; otherwise, one or more of the <a href="https://msdn.microsoft.com/7f99fb6c-32f2-4fd8-ad11-3ad84d17c5c1">KNOWN_FOLDER_FLAG</a> values.


### -param ppszPath [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated buffer that contains the path. The calling application is responsible for calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to free this resource when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Equivalent to <a href="https://msdn.microsoft.com/5434c744-484b-4c34-9a76-dddbcb81eb29">SHGetKnownFolderPath</a>





## -see-also




<a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>



<a href="https://msdn.microsoft.com/5434c744-484b-4c34-9a76-dddbcb81eb29">SHGetKnownFolderPath</a>
 

 

