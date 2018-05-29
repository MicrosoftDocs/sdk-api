---
UID: NF:propvarutil.VariantToStrRet
title: VariantToStrRet function
author: windows-sdk-content
description: If the source variant is a VT_BSTR, extracts string and places it into a STRRET structure.
old-location: properties\VariantToStrRet.htm
old-project: properties
ms.assetid: dfc1f52e-58c6-48fd-8da9-1d4d5115912c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: VariantToStrRet, VariantToStrRet function [Windows Properties], _shell_VariantToStrRet, properties.VariantToStrRet, propvarutil/VariantToStrRet, shell.VariantToStrRet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	VariantToStrRet
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VariantToStrRet function


## -description


If the source variant is a VT_BSTR, extracts string and places it into a <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param pstrret [out]

Type: <b><a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a>*</b>

Pointer to the extracted string if one exists.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



