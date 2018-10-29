---
UID: NF:oleauto.VarFix
title: VarFix function
author: windows-sdk-content
description: Returns the integer portion of a variant.
old-location: automat\varfix.htm
tech.root: automat
ms.assetid: d90f37c7-87a8-4800-901c-d2aa3e5d838b
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: VarFix, VarFix function [Automation], _oa96_VarFix, automat.varfix, oleauto/VarFix
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
 - VarFix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VarFix function


## -description


Returns the integer portion of a variant.


## -parameters




### -param pvarIn [in]

The variant.


### -param pvarResult [out]

The result variant.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the variant is negative, then the first negative integer greater than or equal to the variant is returned.



