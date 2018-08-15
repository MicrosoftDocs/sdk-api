---
UID: NF:oleauto.DispCallFunc
title: DispCallFunc function
author: windows-sdk-content
description: Low-level helper for Invoke that provides machine independence for customized Invoke.
old-location: automat\dispcallfunc.htm
old-project: automat
ms.assetid: 9a16d4e4-a03d-459d-a2ec-3258499f6932
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DispCallFunc, DispCallFunc function [Automation], _oa96_DispCallFunc, automat.dispcallfunc, oleauto/DispCallFunc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - DispCallFunc
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# DispCallFunc function


## -description


Low-level helper for <a href="https://msdn.microsoft.com/964ade8e-9d8a-4d32-bd47-aa678912a54d">Invoke</a> that provides machine independence for customized <b>Invoke</b>.


## -parameters




### -param pvInstance

An instance of the interface described by this type description.



### -param oVft

For FUNC_VIRTUAL functions, specifies the offset in the VTBL.




### -param cc

The calling convention. One of the CALLCONV values, such as CC_STDCALL.


### -param vtReturn

The variant type of the function return value. Use VT_EMPTY to represent void.




### -param cActuals

The number of function parameters.


### -param prgvt

An array of variant types of the function parameters.


### -param prgpvarg

The function parameters.


### -param pvargResult

The function result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



