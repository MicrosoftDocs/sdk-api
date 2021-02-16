---
UID: NF:propidl.IPropertySetStorage.Open
title: IPropertySetStorage::Open (propidl.h)
description: Opens a property set contained in the property set storage object.
helpviewer_keywords: ["IPropertySetStorage interface [Structured Storage]","Open method","IPropertySetStorage.Open","IPropertySetStorage::Open","Open","Open method [Structured Storage]","Open method [Structured Storage]","IPropertySetStorage interface","_stg_ipropertysetstorage_open","propidl/IPropertySetStorage::Open","stg.ipropertysetstorage_open"]
old-location: stg\ipropertysetstorage_open.htm
tech.root: Stg
ms.assetid: a0e2239f-b908-460a-98e8-c805c1d84def
ms.date: 12/05/2018
ms.keywords: IPropertySetStorage interface [Structured Storage],Open method, IPropertySetStorage.Open, IPropertySetStorage::Open, Open, Open method [Structured Storage], Open method [Structured Storage],IPropertySetStorage interface, _stg_ipropertysetstorage_open, propidl/IPropertySetStorage::Open, stg.ipropertysetstorage_open
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
 - IPropertySetStorage::Open
 - propidl/IPropertySetStorage::Open
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
 - IPropertySetStorage.Open
---

# IPropertySetStorage::Open


## -description

The <b>Open</b> method opens a property set contained in the property set storage object.

## -parameters

### -param rfmtid [in]

The format identifier (FMTID) of the property set to be opened. For more information about well-known and predefined FMTIDs in the Platform SDK, see 
<a href="/windows/desktop/Stg/predefined-property-set-format-identifiers">Predefined Property Set Format Identifiers</a>.

### -param grfMode [in]

The access mode in which the newly created property set is to be opened. These flags are taken from <a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>. Flags that may be used and their meanings in the context of this method are described in the following Remarks section.

### -param ppprstg [out]

A pointer to the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> pointer variable that receives the interface pointer to the requested property storage subobject.

## -returns

This method supports the standard return value E_UNEXPECTED, in addition to the following:

## -remarks

The mode in which the property set is to be opened is specified in the parameter <i>grfMode</i>. These flags are taken from <a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>, but, for this method, legal values and their meanings are as follows (only certain combinations of these flag values are legal).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>STGM_DIRECT</td>
<td>Opens the property set without an additional level of transaction nesting. This is the default (the behavior if neither STGM_DIRECT nor STGM_TRANSACTED is specified).</td>
</tr>
<tr>
<td>STGM_TRANSACTED</td>
<td>Opens the property set with an additional level of transaction nesting (beyond the transaction, if any, on this property set storage object). Transacted mode is available only for nonsimple property sets. Changes in the property set must be committed with a call to <a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-commit">IPropertyStorage::Commit</a> before they are visible to the transaction on this property set storage.</td>
</tr>
<tr>
<td>STGM_READ</td>
<td>Opens the property set with read access. Read permission is required on the property set storage.</td>
</tr>
<tr>
<td>STGM_WRITE</td>
<td>Opens the property set with write access. Not all implementations of 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> support this mode.</td>
</tr>
<tr>
<td>STGM_READWRITE</td>
<td>Opens the property set with read and write access. Be aware that this flag is not the binary OR of the values STGM_READ and STGM_WRITE.</td>
</tr>
<tr>
<td>STGM_SHARE_DENY_NONE</td>
<td>Subsequent openings of the property set from this property set storage are not denied read or write access. (Not available in all implementations.)</td>
</tr>
<tr>
<td>STGM_SHARE_DENY_READ</td>
<td>Subsequent openings of the property set from this property set storage are denied read access. Not available in all implementations.</td>
</tr>
<tr>
<td>STGM_SHARE_DENY_WRITE</td>
<td>Subsequent openings of the property set from this property set storage are denied write access. This value is typically used in the transacted mode to prevent making unnecessary copies of an object opened by multiple users. That is, if STGM_TRANSACTED is specified, but this value is not specified, a snapshot is made, whether there are subsequent openings or not. Thus, you can improve performance by specifying this value. Not available in all implementations.</td>
</tr>
<tr>
<td>STGM_SHARE_EXCLUSIVE</td>
<td>Subsequent openings of the property set from this property set storage are not possible. Be aware that this value is not a simple binary OR of the STGM_SHARE_DENY_READ and STGM_SHARE_DENY_WRITE elements.</td>
</tr>
</table>
 

This method is subject to the constraints of the underlying <a href="/windows/desktop/api/objidl/nf-objidl-istorage-openstream">IStorage::OpenStream</a> (for simple property sets) or <a href="/windows/desktop/api/objidl/nf-objidl-istorage-openstorage">IStorage::OpenStorage</a> (for nonsimple property sets). For more information about simple and nonsimple property sets, see 
<a href="/windows/desktop/Stg/storage-vs--stream-for-a-property-set">Storage and Stream Objects for a Property Set</a>. For example, when using the 
<a href="/windows/desktop/Stg/ipropertysetstorage-compound-file-implementation">IPropertySetStorage-Compound File Implementation</a>, you must specify STGM_SHARE_EXCLUSIVE in the <i>grfMode</i> parameter to <b>IPropertySetStorage::Open</b>. Conversely, if using the 
<a href="/windows/desktop/Stg/ipropertysetstorage-stand-alone-implementation">IPropertySetStorage-Stand-alone Implementation</a>, <b>IPropertySetStorage::Open</b> is subject to constraints that apply to the caller-specified 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>.

## -see-also

<a href="/windows/desktop/Stg/enumall-sample">EnumAll Sample</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-create">IPropertySetStorage::Create</a>



<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>



<a href="/windows/desktop/Stg/samples">Samples</a>



<a href="/windows/desktop/Stg/writeread-sample">WriteRead Sample</a>