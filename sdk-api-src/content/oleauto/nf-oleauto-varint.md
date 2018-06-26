---
UID: NF:oleauto.VarInt
title: VarInt function
author: windows-sdk-content
description: Returns the integer portion of a variant.
old-location: automat\varint.htm
old-project: automat
ms.assetid: 96a9a158-d822-4cde-80c5-ea66f0fa4f1f
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: VarInt, VarInt function [Automation], _oa96_VarInt, automat.varint, oleauto/VarInt
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
 - VarInt
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# VarInt function


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



If the variant is negative, then the first negative integer less than or equal to the variant is returned.



