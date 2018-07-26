---
UID: NF:shobjidl_core.IShellLibrary.GetOptions
title: IShellLibrary::GetOptions
author: windows-sdk-content
description: Gets the library's options.
old-location: shell\IShellLibrary_GetOptions.htm
old-project: shell
ms.assetid: 1a144505-e977-4db6-8266-c39c1de8a8f9
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: GetOptions, GetOptions method [Windows Shell], GetOptions method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],GetOptions method, IShellLibrary.GetOptions, IShellLibrary::GetOptions, _shell_IShellLibrary_GetOptions, shell.IShellLibrary_GetOptions, shobjidl_core/IShellLibrary::GetOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellLibrary.GetOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellLibrary::GetOptions


## -description


Gets the library's options.


## -parameters




### -param plofOptions [out]

Type: <b><a href="https://msdn.microsoft.com/205c40ff-a4dc-4a57-b51a-1e230fc170dd">LIBRARYOPTIONFLAGS</a>*</b>

The library options for this library. <a href="https://msdn.microsoft.com/205c40ff-a4dc-4a57-b51a-1e230fc170dd">LIBRARYOPTIONFLAGS</a> is a bitwise enumerator, which means that more than one flag could be set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/205c40ff-a4dc-4a57-b51a-1e230fc170dd">LIBRARYOPTIONFLAGS</a>



<a href="https://msdn.microsoft.com/12F6E6AE-2776-408c-B9AC-E885BE93C27F">Library Description Schema</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

