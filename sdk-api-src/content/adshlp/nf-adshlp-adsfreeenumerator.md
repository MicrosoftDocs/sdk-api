---
UID: NF:adshlp.ADsFreeEnumerator
title: ADsFreeEnumerator function (adshlp.h)
description: Frees an enumerator object created with the ADsBuildEnumerator function.
helpviewer_keywords: ["ADsFreeEnumerator","ADsFreeEnumerator function [ADSI]","_ds_adsfreeenumerator","adshlp/ADsFreeEnumerator","adsi.adsfreeenumerator"]
old-location: adsi\adsfreeenumerator.htm
tech.root: adsi
ms.assetid: 0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315
ms.date: 12/05/2018
ms.keywords: ADsFreeEnumerator, ADsFreeEnumerator function [ADSI], _ds_adsfreeenumerator, adshlp/ADsFreeEnumerator, adsi.adsfreeenumerator
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
 - ADsFreeEnumerator
 - adshlp/ADsFreeEnumerator
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
 - ADsFreeEnumerator
---

# ADsFreeEnumerator function


## -description

The <b>ADsFreeEnumerator</b> function frees an enumerator object created with the  <a href="/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator">ADsBuildEnumerator</a> function.

## -parameters

### -param pEnumVariant [in]

Type: <b>IEnumVARIANT*</b>

Pointer to the  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface on the enumerator object to be freed.

## -returns

Type: <b>HRESULT</b>

This method supports standard return values, as well as the following.

## -remarks

The general process for enumerating objects in a container is as follows.

First, create an enumerator object on that container.

Second, retrieve the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface pointer.

Third, call the <a href="/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext">ADsEnumerateNext</a> function to return an enumerated set of elements from the enumerator object.

Fourth, call the <b>ADSFreeEnumerator</b> function to free the enumerator object.

For more information and a code example, see <a href="/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator">ADsBuildEnumerator</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator">ADsBuildEnumerator</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext">ADsEnumerateNext</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>