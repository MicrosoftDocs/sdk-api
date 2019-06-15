---
UID: NF:combaseapi.PropVariantCopy
title: PropVariantCopy function (combaseapi.h)
author: windows-sdk-content
description: The PropVariantCopy function copies the contents of one PROPVARIANT structure to another.
old-location: stg\propvariantcopy.htm
tech.root: Stg
ms.assetid: ee97d3b2-4dec-43c3-b38d-29edc775b82a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PropVariantCopy, PropVariantCopy function [Structured Storage], _stg_propvariantcopy, combaseapi/PropVariantCopy, stg.propvariantcopy
ms.topic: function
req.header: combaseapi.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - PropVariantCopy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropVariantCopy function


## -description


The 
<b>PropVariantCopy</b> function
			copies the contents of one 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure to another.


## -parameters




### -param pvarDest [in, out]

Pointer to an uninitialized 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure that receives the copy.


### -param pvarSrc [in]

Pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure to be copied.


## -returns



This function returns HRESULT.




## -remarks



Copies a 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure by value so the original <i>pvarSrc</i> and new <i>pvarDest</i> parameters may be freed independently with calls to 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-propvariantclear">PropVariantClear</a>. 
<b>PropVariantCopy</b> does not free the destination as the <a href="http://go.microsoft.com/fwlink/p/?linkid=124592">VariantCopy</a> function does. For nonsimple 
<b>PROPVARIANT</b> types such as VT_STREAM, VT_STORAGE, and so forth, which require a subobject, the copy is made by reference. The pointer is copied and 
<a href="_com_iunknown_addref">IUnknown::AddRef</a> is called on it. It is illegal to pass <b>NULL</b> for either <i>pvarDest</i> or <i>pvarSrc</i>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-propvariantclear">PropVariantClear</a>
 

 

