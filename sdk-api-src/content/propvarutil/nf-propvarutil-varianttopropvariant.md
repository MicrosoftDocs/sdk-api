---
UID: NF:propvarutil.VariantToPropVariant
title: VariantToPropVariant function (propvarutil.h)
author: windows-sdk-content
description: Copies the contents of a VARIANT structure to a PROPVARIANT structure.
old-location: properties\VariantToPropVariant.htm
tech.root: properties
ms.assetid: b321d0a5-310a-4a64-8f39-4487602fbd3f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VariantToPropVariant, VariantToPropVariant function [Windows Properties], properties.VariantToPropVariant, propvarutil/VariantToPropVariant, shell.VariantToPropVariant, shell_VariantToPropVariant
ms.topic: function
f1_keywords: 
 - "propvarutil/VariantToPropVariant"
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
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantToPropVariant
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# VariantToPropVariant function


## -description


Copies the contents of a <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure to a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.


## -parameters




### -param pVar [in]

Type: <b>const VARIANT*</b>

Pointer to a source <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.


### -param pPropVar [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. When this function returns, the <b>PROPVARIANT</b> contains the converted information.


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


