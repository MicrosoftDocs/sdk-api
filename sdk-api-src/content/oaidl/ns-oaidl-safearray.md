---
UID: NS:oaidl.tagSAFEARRAY
title: SAFEARRAY (oaidl.h)
description: Represents a safe array.
helpviewer_keywords: ["*LPSAFEARRAY","FADF_AUTO","FADF_BSTR","FADF_DISPATCH","FADF_EMBEDDED","FADF_FIXEDSIZE","FADF_HAVEIID","FADF_HAVEVARTYPE","FADF_RECORD","FADF_RESERVED","FADF_STATIC","FADF_UNKNOWN","FADF_VARIANT","LPSAFEARRAY","LPSAFEARRAY structure pointer [Automation]","SAFEARRAY","SAFEARRAY structure [Automation]","automat.safearray","oaidl/LPSAFEARRAY","oaidl/SAFEARRAY"]
old-location: automat\safearray.htm
tech.root: automat
ms.assetid: 9ec8025b-4763-4526-ab45-390c5d8b3b1e
ms.date: 12/05/2018
ms.keywords: '*LPSAFEARRAY, FADF_AUTO, FADF_BSTR, FADF_DISPATCH, FADF_EMBEDDED, FADF_FIXEDSIZE, FADF_HAVEIID, FADF_HAVEVARTYPE, FADF_RECORD, FADF_RESERVED, FADF_STATIC, FADF_UNKNOWN, FADF_VARIANT, LPSAFEARRAY, LPSAFEARRAY structure pointer [Automation], SAFEARRAY, SAFEARRAY structure [Automation], automat.safearray, oaidl/LPSAFEARRAY, oaidl/SAFEARRAY'
req.header: oaidl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SAFEARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSAFEARRAY
 - oaidl/tagSAFEARRAY
 - SAFEARRAY
 - oaidl/SAFEARRAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - SAFEARRAY
---

# SAFEARRAY structure


## -description

Represents a safe array.

## -struct-fields

### -field cDims

The number of dimensions.

### -field fFeatures

Flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FADF_AUTO"></a><a id="fadf_auto"></a><dl>
<dt><b>FADF_AUTO</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
An array that is allocated on the stack.


</td>
</tr>
<tr>
<td width="40%"><a id="FADF_STATIC"></a><a id="fadf_static"></a><dl>
<dt><b>FADF_STATIC</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
An array that is statically allocated.


</td>
</tr>
<tr>
<td width="40%"><a id="FADF_EMBEDDED"></a><a id="fadf_embedded"></a><dl>
<dt><b>FADF_EMBEDDED</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
An array that is embedded in a structure.


</td>
</tr>
<tr>
<td width="40%"><a id="FADF_FIXEDSIZE"></a><a id="fadf_fixedsize"></a><dl>
<dt><b>FADF_FIXEDSIZE</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
An array that may not be resized or reallocated.


</td>
</tr>
<tr>
<td width="40%"><a id="FADF_RECORD"></a><a id="fadf_record"></a><dl>
<dt><b>FADF_RECORD</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
An array that contains records. When set, there will be a pointer to the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a> interface at negative offset 4 in the array descriptor.


</td>
</tr>
<tr>
<td width="40%"><a id="FADF_HAVEIID"></a><a id="fadf_haveiid"></a><dl>
<dt><b>FADF_HAVEIID</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
An array that has an IID identifying interface. When set, there will be a GUID at negative offset 16 in the safe array descriptor. Flag is set only when FADF_DISPATCH or FADF_UNKNOWN is also set. 


</td>
</tr>
<tr>
<td width="40%"><a id="FADF_HAVEVARTYPE"></a><a id="fadf_havevartype"></a><dl>
<dt><b>FADF_HAVEVARTYPE</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
An array that has a variant type. The variant type can be retrieved with <a href="/previous-versions/windows/desktop/automat/vartype">SafeArrayGetVartype</a>. 


</td>
</tr>
<tr>
<td width="40%"><a id="FADF_BSTR"></a><a id="fadf_bstr"></a><dl>
<dt><b>FADF_BSTR</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
An array of BSTRs.


</td>
</tr>
<tr>
<td width="40%"><a id="FADF_UNKNOWN"></a><a id="fadf_unknown"></a><dl>
<dt><b>FADF_UNKNOWN</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
An array of IUnknown*.


</td>
</tr>
<tr>
<td width="40%"><a id="FADF_DISPATCH"></a><a id="fadf_dispatch"></a><dl>
<dt><b>FADF_DISPATCH</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
An array of IDispatch*.


</td>
</tr>
<tr>
<td width="40%"><a id="FADF_VARIANT"></a><a id="fadf_variant"></a><dl>
<dt><b>FADF_VARIANT</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
An array of VARIANTs.


</td>
</tr>
<tr>
<td width="40%"><a id="FADF_RESERVED"></a><a id="fadf_reserved"></a><dl>
<dt><b>FADF_RESERVED</b></dt>
<dt>0xF008</dt>
</dl>
</td>
<td width="60%">
Bits reserved for future use.


</td>
</tr>
</table>

### -field cbElements

The size of an array element.

### -field cLocks

The number of times the array has been locked without a corresponding unlock.

### -field pvData

The data.

### -field rgsabound

One bound for each dimension.

## -remarks

The array <b>rgsabound</b> is stored with the left-most dimension in rgsabound[0] and the right-most dimension in <code>rgsabound[cDims - 1]</code>. If an array was specified in a C-like syntax as a [2][5], it would have two elements in the <b>rgsabound</b> vector. Element 0 has an <b>lLbound</b> of 0 and a <b>cElements</b> of 2. Element 1 has an <b>lLbound</b> of 0 and a <b>cElements</b> of 5.



The <b>fFeatures</b> flags describe attributes of an array that can affect how the array is released. The <b>fFeatures</b> field describes what type of data is stored in the <b>SAFEARRAY</b> and how the array is allocated. This allows freeing the array without referencing its containing variant.


#### Thread Safety

All public static members of the <b>SAFEARRAY</b> data type are thread safe. Instance members are not guaranteed to be thread safe.



For example, consider an application that uses the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraylock">SafeArrayLock</a> and <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayunlock">SafeArrayUnlock</a> functions. If these functions are called concurrently from different threads on the same <b>SAFEARRAY</b> data type instance, an inconsistent lock count may be created. This will eventually cause the <b>SafeArrayUnlock</b> function to return E_UNEXPECTED. You can prevent this by providing your own synchronization code.