---
UID: NF:adshlp.ADsEnumerateNext
title: ADsEnumerateNext function (adshlp.h)
description: The ADsEnumerateNext function enumerates through a specified number of elements from the current cursor position of the enumerator.
helpviewer_keywords: ["ADsEnumerateNext","ADsEnumerateNext function [ADSI]","_ds_adsenumeratenext","adshlp/ADsEnumerateNext","adsi.adsenumeratenext"]
old-location: adsi\adsenumeratenext.htm
tech.root: adsi
ms.assetid: 9bfc98a5-f4f0-4127-89c9-b8ed01bfde4e
ms.date: 12/05/2018
ms.keywords: ADsEnumerateNext, ADsEnumerateNext function [ADSI], _ds_adsenumeratenext, adshlp/ADsEnumerateNext, adsi.adsenumeratenext
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ADsEnumerateNext
 - adshlp/ADsEnumerateNext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ADsEnumerateNext
---

# ADsEnumerateNext function


## -description

The <b>ADsEnumerateNext</b> function enumerates through a specified number of elements from the current cursor position of the enumerator. When the operation succeeds, the function returns the enumerated set of elements in a variant array. The number of returned elements can be smaller than the specified number.

## -parameters

### -param pEnumVariant [in]

Type: <b>IEnumVARIANT*</b>

Pointer to the  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface on the enumerator object.

### -param cElements [in]

Type: <b>ULONG</b>

Number of elements requested.

### -param pvar [out]

Type: <b>VARIANT*</b>

Pointer to the array of elements retrieved.

### -param pcElementsFetched [out]

Type: <b>ULONG*</b>

Actual number of elements retrieved, which can be smaller than the number of elements requested.

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values.

For more information about other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The general process to enumerate objects in a container involves the following:

First, create an enumerator object on that container.

Second, retrieve the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface pointer.

Third, call the <b>ADsEnumerateNext</b> function to return an enumerated set of elements from the enumerator object.

Fourth, call the <a href="/windows/desktop/api/adshlp/nf-adshlp-adsfreeenumerator">ADSFreeEnumerator</a> function to free the enumerator object.

For more information and a code example, see the  <a href="/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator">ADsBuildEnumerator</a> topic.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator">ADsBuildEnumerator</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsfreeenumerator">ADsFreeEnumerator</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>