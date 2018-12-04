---
UID: NF:oleauto.VarPow
title: VarPow function
author: windows-sdk-content
description: Returns the result of performing the power function with two variants.
old-location: automat\varpow.htm
tech.root: automat
ms.assetid: 80e19d25-94cf-49f8-b49f-9cda14d0ee4b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: VarPow, VarPow function [Automation], _oa96_VarPow, automat.varpow, oleauto/VarPow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarPow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VarPow function


## -description


Returns the result of performing the power function with two variants.


## -parameters




### -param pvarLeft [in]

The first variant.


### -param pvarRight [in]

The second variant.


### -param pvarResult [out]

The result variant.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Returns the result of <i>pvarLeft</i> to the power of <i>pvarRight</i>.




