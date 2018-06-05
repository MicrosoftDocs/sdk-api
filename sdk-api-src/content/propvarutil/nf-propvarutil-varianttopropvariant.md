---
UID: NF:propvarutil.VariantToPropVariant
title: VariantToPropVariant function
author: windows-sdk-content
description: Copies the contents of a VARIANT structure to a PROPVARIANT structure.
old-location: properties\VariantToPropVariant.htm
old-project: properties
ms.assetid: b321d0a5-310a-4a64-8f39-4487602fbd3f
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: VariantToPropVariant, VariantToPropVariant function [Windows Properties], properties.VariantToPropVariant, propvarutil/VariantToPropVariant, shell.VariantToPropVariant, shell_VariantToPropVariant
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	VariantToPropVariant
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VariantToPropVariant function


## -description


Copies the contents of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param pVar [in]

Type: <b>const VARIANT*</b>

Pointer to a source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


### -param pPropVar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. When this function returns, the <b>PROPVARIANT</b> contains the converted information.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The following cannot be handled by this function.
                
                

<ul>
<li>VT_BYREF | VT_DATE</li>
<li>VT_BYREF | VT_BSTR</li>
<li>VT_BYREF | VT_UNKNOWN</li>
</ul>


