---
UID: NF:oleauto.VarCyFix
title: VarCyFix function
author: windows-driver-content
description: Retrieves the integer portion of a variant of type currency.
old-location: automat\varcyfix.htm
old-project: automat
ms.assetid: b688530b-e911-4f48-8dab-bb1ca1c6e718
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: VarCyFix, VarCyFix function [Automation], _oa96_VarCyFix, automat.varcyfix, oleauto/VarCyFix
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
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	VarCyFix
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VarCyFix function


## -description


Retrieves the integer portion of a variant of type currency.


## -parameters




### -param cyIn [in]

The currency variant.


### -param pcyResult [out]

The resulting variant. If the variant is negative, then the first negative integer greater than or equal to the variant is returned.



## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



