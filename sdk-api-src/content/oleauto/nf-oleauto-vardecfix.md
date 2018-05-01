---
UID: NF:oleauto.VarDecFix
title: VarDecFix function
author: windows-driver-content
description: Retrieves the integer portion of a variant of type decimal.
old-location: automat\vardecfix.htm
old-project: automat
ms.assetid: 714567f9-7159-4081-a5d2-afd4da789961
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: VarDecFix, VarDecFix function [Automation], _oa96_VarDecFix, automat.vardecfix, oleauto/VarDecFix
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
-	VarDecFix
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# VarDecFix function


## -description


Retrieves the integer portion of a variant of type decimal.


## -parameters




### -param pdecIn [in]

The decimal variant.


### -param pdecResult [out]

The resulting variant. If the variant is negative, then the first negative integer greater than or equal to the variant is returned.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



