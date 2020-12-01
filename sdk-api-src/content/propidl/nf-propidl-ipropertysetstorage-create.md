---
UID: NF:propidl.IPropertySetStorage.Create
title: IPropertySetStorage::Create (propidl.h)
description: Creates and opens a new property set in the property set storage object.
helpviewer_keywords: ["Create","Create method [Structured Storage]","Create method [Structured Storage]","IPropertySetStorage interface","IPropertySetStorage interface [Structured Storage]","Create method","IPropertySetStorage.Create","IPropertySetStorage::Create","_stg_ipropertysetstorage_create","propidl/IPropertySetStorage::Create","stg.ipropertysetstorage_create"]
old-location: stg\ipropertysetstorage_create.htm
tech.root: Stg
ms.assetid: 9307788d-bce6-4025-8043-8b68e874a62b
ms.date: 12/05/2018
ms.keywords: Create, Create method [Structured Storage], Create method [Structured Storage],IPropertySetStorage interface, IPropertySetStorage interface [Structured Storage],Create method, IPropertySetStorage.Create, IPropertySetStorage::Create, _stg_ipropertysetstorage_create, propidl/IPropertySetStorage::Create, stg.ipropertysetstorage_create
req.header: propidl.h
req.include-header: Objbase.h
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
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertySetStorage::Create
 - propidl/IPropertySetStorage::Create
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IPropertySetStorage.Create
---

# IPropertySetStorage::Create


## -description

The <b>Create</b> method 
			creates and opens a new property set in the property set storage object.

## -parameters

### -param rfmtid [in]

The FMTID of the property set to be created. For information about FMTIDs that are well-known and predefined in the Platform SDK, see 
<a href="/windows/desktop/Stg/predefined-property-set-format-identifiers">Predefined Property Set Format Identifiers</a>.

### -param pclsid [in]

A pointer to the initial class identifier CLSID for this property set. May be <b>NULL</b>, in which case it is set to all zeroes. The CLSID is the CLSID of a class that displays and/or provides programmatic access to the property values. If there is no such class, it is recommended that the FMTID be used.

### -param grfFlags [in]

The values from <a href="/windows/desktop/Stg/propsetflag-constants">PROPSETFLAG Constants</a>.

### -param grfMode [in]

An access mode in which the newly created property set is to be opened, taken from certain values of <a href="/windows/desktop/Stg/stgm-constants">STGM_Constants</a>, as described in the following Remarks section.

### -param ppprstg [out]

A pointer to the output variable that receives the <a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface pointer.

## -returns

This method supports the standard return value E_UNEXPECTED, as well as the following:

## -remarks

<b>IPropertySetStorage::Create</b> creates and opens a new property set subobject (supporting the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface) contained in this property set storage object. The property set automatically contains code page and locale ID properties. These are set to the Unicode and the current user default, respectively.

The <i>grfFlags</i> parameter is a combination of values taken from <a href="/windows/desktop/Stg/propsetflag-constants">PROPSETFLAG Constants</a>. If the PROPSETFLAG_ANSI value from this enumeration is used, the code page is set to the current system default, rather than Unicode.

The <i>grfMode</i> parameter specifies the access mode in which the newly created set is to be opened. Values for this parameter are as in the <i>grfMode</i> parameter to 
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-open">IPropertySetStorage::Open</a>, with the addition of the values listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>STGM_FAILIFTHERE</td>
<td>If another property set with the specified <i>fmtid</i> parameter exists, the call fails. This is the default action; that is, unless STGM_CREATE is specified, STGM_FAILIFTHERE is implied.</td>
</tr>
<tr>
<td>STGM_CREATE</td>
<td>If another property set with the specified <i>fmtid</i> parameter already exists, it is removed and replaced with this new one.</td>
</tr>
</table>
 

The created property set is simple by default, but the caller may request a nonsimple property set by specifying the PROPSETFLAG_NONSIMPLE value in the <i>grfFlags</i> parameter. For more information about simple and nonsimple property sets, see 
<a href="/windows/desktop/Stg/storage-vs--stream-for-a-property-set">Storage and Stream Objects for a Property Set</a>.

This method is subject to the constraints of the underlying <a href="/windows/desktop/api/objidl/nf-objidl-istorage-createstream">IStorage::CreateStream</a> (for simple property sets) or <a href="/windows/desktop/api/objidl/nf-objidl-istorage-createstorage">IStorage::CreateStorage</a> (for nonsimple property sets). For example, when using the 
<a href="/windows/desktop/Stg/ipropertysetstorage-compound-file-implementation">IPropertySetStorage-Compound File Implementation</a>, specify STGM_SHARE_EXCLUSIVE in the <i>grfMode</i> parameter to <b>IPropertySetStorage::Create</b>. Conversely, if  using the 
<a href="/windows/desktop/Stg/ipropertysetstorage-stand-alone-implementation">IPropertySetStorage-Stand-alone Implementation</a>, <b>IPropertySetStorage::Create</b> is subject to constraints that apply to the caller-specified 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>.

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-open">IPropertySetStorage::Open</a>



<a href="/windows/desktop/Stg/propsetflag-constants">PROPSETFLAG Constants</a>



<a href="/windows/desktop/Stg/samples">Samples</a>



<a href="/windows/desktop/Stg/stgcreatepropsetstg-sample">StgCreatePropSetStg Sample</a>



<a href="/windows/desktop/Stg/writeread-sample">WriteRead Sample</a>