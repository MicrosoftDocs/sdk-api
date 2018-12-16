---
UID: NF:dcomp.DCompositionCreateDevice3
title: DCompositionCreateDevice3 function
author: windows-sdk-content
description: Creates a new DirectComposition device object, which can be used to create other DirectComposition objects.
old-location: directcomp\dcompositioncreatedevice3.htm
tech.root: directcomp
ms.assetid: 5EF8F6E9-7632-42B4-A589-10CD4ABC7695
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DCompositionCreateDevice3, DCompositionCreateDevice3 function [DirectComposition], dcomp/DCompositionCreateDevice3, directcomp.dcompositioncreatedevice3
ms.topic: function
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
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
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dcomp.dll
api_name:
 - DCompositionCreateDevice3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DCompositionCreateDevice3 function


## -description


Creates a new DirectComposition device object, which can be used to create other DirectComposition objects.


## -parameters




### -param renderingDevice [in, optional]

Type: <b>IUnknown*</b>

An optional pointer to a DirectX device to be used to create DirectComposition surface objects. Must be a pointer to an object implementing the <a href="https://msdn.microsoft.com/en-us/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a> or <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> interfaces.


### -param iid [in]

Type: <b>REFIID</b>

The identifier of the interface to retrieve. This must be one of __uuidof(IDCompositionDevice) or __uuidof(IDCompositionDesktopDevice).


### -param dcompositionDevice [out]

Type: <b>void**</b>

Receives an interface pointer to the newly created device object. The pointer is of the type specified by the <i>iid</i> parameter. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



