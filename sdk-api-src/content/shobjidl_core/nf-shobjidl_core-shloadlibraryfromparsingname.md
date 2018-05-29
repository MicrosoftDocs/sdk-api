---
UID: NF:shobjidl_core.SHLoadLibraryFromParsingName
title: SHLoadLibraryFromParsingName function
author: windows-sdk-content
description: Creates and loads an IShellLibrary object for a specified path.
old-location: shell\SHLoadLibraryFromParsingName.htm
old-project: shell
ms.assetid: 49433938-d31e-49f8-9dc7-3df5fb3bfcad
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHLoadLibraryFromParsingName, SHLoadLibraryFromParsingName function [Windows Shell], _shell_SHLoadLibraryFromParsingName, shell.SHLoadLibraryFromParsingName, shobjidl_core/SHLoadLibraryFromParsingName
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shobjidl_core.h
api_name:
-	SHLoadLibraryFromParsingName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# SHLoadLibraryFromParsingName function


## -description


Creates and loads an <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object for a specified path.


## -parameters




### -param pszParsingName [in]

Type: <b>PCWSTR</b>

The path for which to load the <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object.


### -param grfMode [in]

Type: <b>DWORD</b>

One or more storage medium flags that specify access and sharing modes for the library object. Commonly specified flags are <b>STGM_READ</b> or <b>STGM_READWRITE</b>. For more information, see <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IShellLibrary.


### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

This is an inline helper function that wraps the <a href="https://msdn.microsoft.com/5dd2c197-8846-481f-b51e-ea0a93fd5e9b">IShellLibrary::LoadLibraryFromItem</a> method.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/5dd2c197-8846-481f-b51e-ea0a93fd5e9b">IShellLibrary::LoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/3fc1147e-6338-4fec-b20d-db5eb1303fe1">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/7e682a2e-5140-49ad-88de-ac681025aca4">SHCreateLibrary</a>



<a href="https://msdn.microsoft.com/9692f9d1-1504-43d0-9eb1-3759a8e2b42d">SHLoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/9486252b-9aaf-4daf-b307-5a5adddfaa99">SHLoadLibraryFromKnownFolder</a>
 

 

