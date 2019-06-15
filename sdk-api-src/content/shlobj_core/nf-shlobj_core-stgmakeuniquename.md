---
UID: NF:shlobj_core.StgMakeUniqueName
title: StgMakeUniqueName function (shlobj_core.h)
author: windows-sdk-content
description: Creates a unique name for a stream or storage object from a template.
old-location: shell\StgMakeUniqueName.htm
tech.root: shell
ms.assetid: d45ec25c-359b-46f8-b0f6-5888525c7349
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: StgMakeUniqueName, StgMakeUniqueName function [Windows Shell], _shell_StgMakeUniqueName, shell.StgMakeUniqueName, shlobj_core/StgMakeUniqueName
ms.topic: function
f1_keywords: ["shlobj_core/StgMakeUniqueName"]
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - StgMakeUniqueName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StgMakeUniqueName function


## -description


Creates a unique name for a stream or storage object from a template.


## -parameters




### -param pstgParent [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> object.


### -param pszFileSpec [in]

Type: <b>PCWSTR</b>

The format or template for the name of the stream or storage object.


### -param grfMode [in]

Type: <b>DWORD</b>

The access mode to use when opening the stream or storage object. For more information and descriptions of the possible values, see STGM Constants.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IStorage or IID_IStream.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> or <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is recommended that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.



