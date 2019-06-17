---
UID: NF:propvarutil.PropVariantGetElementCount
title: PropVariantGetElementCount function (propvarutil.h)
author: windows-sdk-content
description: Retrieves the element count of a PROPVARIANT structure.
old-location: properties\PropVariantGetElementCount.htm
tech.root: properties
ms.assetid: 1d02f06e-f90b-40f2-923b-a89d2d4d535c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PropVariantGetElementCount, PropVariantGetElementCount function [Windows Properties], _shell_PropVariantGetElementCount, properties.PropVariantGetElementCount, propvarutil/PropVariantGetElementCount, shell.PropVariantGetElementCount
ms.topic: function
f1_keywords: ["propvarutil/PropVariantGetElementCount"]
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
 - PropVariantGetElementCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# PropVariantGetElementCount function


## -description


Retrieves the element count of a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to the source <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure.


## -returns



Type: <b>ULONG</b>

Returns the element count of a VT_VECTOR or VT_ARRAY value: for single values, returns 1; for empty structures, returns 0.




## -remarks



This function works for all valid <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> types. See <b>PROPVARIANT</b> for the valid type combinations.

This function is useful to get the count of elements to iterate through using a looping statement, especially for iterations that call functions such as <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetuint32elem">PropVariantGetUInt32Elem</a> or <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelem">PropVariantGetElem</a>.



