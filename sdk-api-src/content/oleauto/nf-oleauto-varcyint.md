---
UID: NF:oleauto.VarCyInt
title: VarCyInt function
author: windows-sdk-content
description: Retrieves the integer portion of a variant of type currency.
old-location: automat\varcyint.htm
tech.root: automat
ms.assetid: 234c8407-93c9-49bd-aae7-d526d5f5e34c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: VarCyInt, VarCyInt function [Automation], _oa96_VarCyInt, automat.varcyint, oleauto/VarCyInt
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
 - VarCyInt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VarCyInt function


## -description


Retrieves the integer portion of a variant of type currency.


## -parameters




### -param cyIn [in]

The currency variant.


### -param pcyResult [out]

The resulting variant. If the variant is negative then the first negative integer less than or equal to the variant is returned.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



