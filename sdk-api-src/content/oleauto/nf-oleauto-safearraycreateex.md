---
UID: NF:oleauto.SafeArrayCreateEx
title: SafeArrayCreateEx function (oleauto.h)
description: Creates and returns a safe array descriptor from the specified VARTYPE, number of dimensions and bounds.
helpviewer_keywords: ["SafeArrayCreateEx","SafeArrayCreateEx function [Automation]","_oa96_SafeArrayCreateEx","automat.safearraycreateex","oleauto/SafeArrayCreateEx"]
old-location: automat\safearraycreateex.htm
tech.root: automat
ms.assetid: 63117428-6676-4fb5-a0ae-7e3b22546d77
ms.date: 12/05/2018
ms.keywords: SafeArrayCreateEx, SafeArrayCreateEx function [Automation], _oa96_SafeArrayCreateEx, automat.safearraycreateex, oleauto/SafeArrayCreateEx
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SafeArrayCreateEx
 - oleauto/SafeArrayCreateEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayCreateEx
---

# SafeArrayCreateEx function


## -description

Creates and returns a safe array descriptor from the specified VARTYPE, number of dimensions and bounds.

## -parameters

### -param vt [in]

The base type or the VARTYPE of each element of the array. The FADF_RECORD flag can be set for a variant type VT_RECORD, The FADF_HAVEIID flag can be set for VT_DISPATCH or VT_UNKNOWN, and FADF_HAVEVARTYPE can be set for all other VARTYPEs.

### -param cDims [in]

The number of dimensions in the array.

### -param rgsabound [in]

A vector of bounds (one for each dimension) to allocate for the array.

### -param pvExtra [in]

the type information of the user-defined type, if you are creating a safe array of user-defined types. If the vt parameter is VT_RECORD, then <i>pvExtra</i> will be a pointer to an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a> describing the record. If the <i>vt</i> parameter is VT_DISPATCH or VT_UNKNOWN, then <i>pvExtra</i> will contain a pointer to a GUID representing the type of interface being passed to the array.

## -returns

A safe array descriptor, or null if the array could not be created.

## -remarks

If the VARTYPE is VT_RECORD then <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraysetrecordinfo">SafeArraySetRecordInfo</a> is called. If the VARTYPE is VT_DISPATCH or VT_UNKNOWN then the elements of the array must contain interfaces of the same type. Part of the process of marshaling this array to other processes does include generating the proxy/stub code of the IID pointed to by the <i>pvExtra</i> parameter. To actually pass heterogeneous interfaces one will need to specify either IID_IUnknown or IID_IDispatch in <i>pvExtra</i> and provide some other means for the caller to identify how to query for the actual interface.


#### Examples

The following example describes how a safe array of user-defined types is stored into a variant of type VT_RECORD.


```cpp
SAFEARRAYBOUND * sab;
sab.cElements = 2;
sab.lLbound = 0;
hresult hr;

SAFEARRAY Sa;
Sa = SafeArrayCreateEx(VT_RECORD, 1, &sab, pRecInfo);
if (Sa == NULL)
   return E_OUTOFMEMORY;

PVOID pvData;
hr = SafeArrayAccessData(Sa, &pvData);
if (FAILED(hr)) {
   SafeArrayDestroy(Sa);
   return hr;
}

TEST * pTest;
pTest = (TEST *)pvData;
pTest[0] = a;
pTest[1] = b;
hr = SafeArrayUnaccessData(Sa);
if (FAILED(hr)) {
   SafeArrayDestroy(Sa);
   return hr;
}

VariantInit(&variant);
V_VT(&variant) = VT_ARRAY|VT_RECORD;
V_ARRAY(&variant) = Sa;
```