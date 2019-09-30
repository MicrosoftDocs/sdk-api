---
UID: NF:shlobj_core.SHCoCreateInstance
title: SHCoCreateInstance function (shlobj_core.h)
author: windows-sdk-content
description: SHCoCreateInstance may be altered or unavailable. Instead, use CoCreateInstance.
old-location: shell\SHCoCreateInstance.htm
tech.root: shell
ms.assetid: 334fc581-29b2-4576-94ec-7dd3d6e0020b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SHCoCreateInstance, SHCoCreateInstance function [Windows Shell], _win32_SHCoCreateInstance, shell.SHCoCreateInstance, shlobj_core/SHCoCreateInstance
ms.topic: function
f1_keywords: 
 - "shlobj_core/SHCoCreateInstance"
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-shell-shellcom-l1-1-0.dll
 - KernelBase.dll
api_name:
 - SHCoCreateInstance
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHCoCreateInstance function


## -description


<p class="CCE_Message">[<b>SHCoCreateInstance</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>.]

Creates Component Object Model (COM) objects that are implemented in Shell32.dll.


## -parameters




### -param pszCLSID [in, optional]

Type: <b>PCWSTR</b>

A pointer to a string to convert to a CLSID. If <b>NULL</b>, <i>pclsid</i> is used as the CLSID.


### -param pclsid [in, optional]

Type: <b>const CLSID*</b>

The CLSID to create.


### -param pUnkOuter [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to outer <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>. Used for aggregation.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>.


### -param ppv [out]

Type: <b>void**</b>

When this function returns successfully, receives the interface pointer requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



We recommend that you use the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.



