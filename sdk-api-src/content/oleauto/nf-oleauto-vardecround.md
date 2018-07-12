---
UID: NF:oleauto.VarDecRound
title: VarDecRound function
author: windows-sdk-content
description: Rounds a variant of type decimal to the specified number of decimal places.
old-location: automat\vardecround.htm
old-project: automat
ms.assetid: 264914c6-2f47-4e99-b3bb-a2c510906954
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: VarDecRound, VarDecRound function [Automation], _oa96_VarDecRound, automat.vardecround, oleauto/VarDecRound
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
 - VarDecRound
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# VarDecRound function


## -description


Rounds a variant of type decimal to the specified number of decimal places. 


## -parameters




### -param pdecIn [in]

The variant to round.


### -param cDecimals [in]

The number of decimal places.


### -param pdecResult [out]

The resulting variant.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



