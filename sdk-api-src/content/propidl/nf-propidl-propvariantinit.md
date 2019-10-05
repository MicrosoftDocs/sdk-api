---
UID: NF:propidl.PropVariantInit
title: PropVariantInit macro (propidl.h)
author: windows-sdk-content
description: The PropVariantInit function initializes a PROPVARIANT structure.Note  This function is implemented as a macro, available by including the provided ole2.h header file.
old-location: stg\propvariantinit.htm
tech.root: Stg
ms.assetid: 8c1bf6ac-2b15-4a05-8cb9-a07d1437017c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PropVariantInit, PropVariantInit function [Structured Storage], _stg_propvariantinit, propidl/PropVariantInit, stg.propvariantinit
ms.topic: macro
f1_keywords: 
 - "propidl/PropVariantInit"
dev_langs:
 - c++
req.header: propidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PropIdl.h
api_name:
 - PropVariantInit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropVariantInit macro


## -description


The <b>PropVariantInit</b> function
			initializes a 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.
<div class="alert"><b>Note</b>  This function is implemented as a macro, available by including the provided ole2.h header file. This function is not exported from any system-provided DLL.</div><div> </div>

## -parameters




### -param pvar [out]

Pointer to an uninitialized 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that is initialized.


## -remarks



Initializes a 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure, and sets its type to VT_EMPTY. <b>PropVariantInit</b> should not be used to clear a <b>PROPVARIANT</b> structure that contains data; for example, when it contains the result of a call to 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readmultiple">IPropertyStorage::ReadMultiple</a>. Such a 
<b>PROPVARIANT</b> structure should be cleared using the 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-propvariantclear">PropVariantClear</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-propvariantclear">PropVariantClear</a>
 

 

