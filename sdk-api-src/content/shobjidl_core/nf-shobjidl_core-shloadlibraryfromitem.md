---
UID: NF:shobjidl_core.SHLoadLibraryFromItem
title: SHLoadLibraryFromItem function (shobjidl_core.h)
author: windows-sdk-content
description: Creates and loads an IShellLibrary object from a specified library definition file.
old-location: shell\SHLoadLibraryFromItem.htm
tech.root: shell
ms.assetid: 9692f9d1-1504-43d0-9eb1-3759a8e2b42d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SHLoadLibraryFromItem, SHLoadLibraryFromItem function [Windows Shell], _shell_SHLoadLibraryFromItem, shell.SHLoadLibraryFromItem, shobjidl_core/SHLoadLibraryFromItem
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SHLoadLibraryFromItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHLoadLibraryFromItem function


## -description


Creates and loads an <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object from a specified library definition file.


## -parameters




### -param psiLibrary [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

An <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object for the library definition file to load.


### -param grfMode [in]

Type: <b>DWORD</b>

One or more storage medium flags that specify access and sharing modes for the library object. Commonly specified flags are <b>STGM_READ</b> or <b>STGM_READWRITE</b>. For more information, see <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a>.


### -param riid [in]

Type: <b>REFIID</b>

The IID for <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>. (See usage remarks.)


### -param ppv [out]

Type: <b>void**</b>

Receives the loaded <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object. (See usage remarks.)


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<h3><a id="Usage"></a><a id="usage"></a><a id="USAGE"></a>Usage</h3>
The <b>IID_PPV_ARGS</b> macro is generally used to generate the <i>riid</i> and <i>ppv</i> parameters for this function. For an example, see <a href="https://msdn.microsoft.com/7e682a2e-5140-49ad-88de-ac681025aca4">SHCreateLibrary</a>.

This is an inline helper function that wraps the <a href="https://msdn.microsoft.com/5dd2c197-8846-481f-b51e-ea0a93fd5e9b">IShellLibrary::LoadLibraryFromItem</a> method.




## -see-also




<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>



<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/5dd2c197-8846-481f-b51e-ea0a93fd5e9b">IShellLibrary::LoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/3fc1147e-6338-4fec-b20d-db5eb1303fe1">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/8fb84a20-d8f2-4c7c-bfb1-a22791b8636a">SHCreateItemWithParent</a>



<a href="https://msdn.microsoft.com/7e682a2e-5140-49ad-88de-ac681025aca4">SHCreateLibrary</a>



<a href="https://msdn.microsoft.com/0ef494c0-81c7-4fbd-9c37-78861d8ac63b">SHGetItemFromObject</a>



<a href="https://msdn.microsoft.com/9486252b-9aaf-4daf-b307-5a5adddfaa99">SHLoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/49433938-d31e-49f8-9dc7-3df5fb3bfcad">SHLoadLibraryFromParsingName</a>
 

 

