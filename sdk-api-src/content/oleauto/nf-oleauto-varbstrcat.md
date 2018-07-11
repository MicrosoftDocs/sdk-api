---
UID: NF:oleauto.VarBstrCat
title: VarBstrCat function
author: windows-sdk-content
description: Concatenates two variants of type BSTR and returns the resulting BSTR.
old-location: automat\varbstrcat.htm
old-project: automat
ms.assetid: e23e1130-dd95-43ec-8ea3-c213fd6b0b25
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: VarBstrCat, VarBstrCat function [Automation], _oa96_VarBstrCat, automat.varbstrcat, oleauto/VarBstrCat
ms.prod: windows
ms.technology: windows-sdk
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
 - VarBstrCat
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# VarBstrCat function


## -description


Concatenates two variants of type BSTR and returns the resulting BSTR.


## -parameters




### -param bstrLeft [in]

The first variant.


### -param bstrRight [in]

The second variant.


### -param pbstrResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



