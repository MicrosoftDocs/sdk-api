---
UID: NF:propidl.IPropertySetStorage.Open
title: IPropertySetStorage::Open
author: windows-sdk-content
description: Opens a property set contained in the property set storage object.
old-location: stg\ipropertysetstorage_open.htm
old-project: Stg
ms.assetid: a0e2239f-b908-460a-98e8-c805c1d84def
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IPropertySetStorage interface [Structured Storage],Open method, IPropertySetStorage.Open, IPropertySetStorage::Open, Open, Open method [Structured Storage], Open method [Structured Storage],IPropertySetStorage interface, _stg_ipropertysetstorage_open, propidl/IPropertySetStorage::Open, stg.ipropertysetstorage_open
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propidl.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PROFILEINFOW, *LPPROFILEINFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IPropertySetStorage.Open
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPropertySetStorage::Open


## -description



			The <b>Open</b> method opens a property set contained in the property set storage object.


## -parameters




### -param rfmtid




### -param grfMode [in]

The access mode in which the newly created property set is to be opened. These flags are taken from <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>. Flags that may be used and their meanings in the context of this method are described in the following Remarks section.


### -param ppprstg






#### - fmtid [in]

The format identifier (FMTID) of the property set to be opened. For more information about well-known and predefined FMTIDs in the Platform SDK, see 
<a href="https://msdn.microsoft.com/cc99ce1b-beb5-4340-91ed-3aed5bdad2bd">Predefined Property Set Format Identifiers</a>.


#### - ppPropStg [out]

A pointer to the 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> pointer variable that receives the interface pointer to the requested property storage subobject.


## -returns




						This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



The mode in which the property set is to be opened is specified in the parameter <i>grfMode</i>. These flags are taken from <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>, but, for this method, legal values and their meanings are as follows (only certain combinations of these flag values are legal).

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
<td>Opens the property set with an additional level of transaction nesting (beyond the transaction, if any, on this property set storage object). Transacted mode is available only for nonsimple property sets. Changes in the property set must be committed with a call to <a href="https://msdn.microsoft.com/00efae8b-023e-425d-b7cd-c40c17d7948e">IPropertyStorage::Commit</a> before they are visible to the transaction on this property set storage.</td>
</tr>
<tr>
<td>STGM_READ</td>
<td>Opens the property set with read access. Read permission is required on the property set storage.</td>
</tr>
<tr>
<td>STGM_WRITE</td>
<td>Opens the property set with write access. Not all implementations of 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> support this mode.</td>
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
 

This method is subject to the constraints of the underlying <a href="https://msdn.microsoft.com/f7bd1f26-e9a3-415d-8cd3-dc34f7ad8feb">IStorage::OpenStream</a> (for simple property sets) or <a href="https://msdn.microsoft.com/f1f0564e-0ecd-4b73-8863-9d6b6746fd02">IStorage::OpenStorage</a> (for nonsimple property sets). For more information about simple and nonsimple property sets, see 
<a href="https://msdn.microsoft.com/d0ca649a-d405-4c34-af02-9c2ca8b2790e">Storage and Stream Objects for a Property Set</a>. For example, when using the 
<a href="https://msdn.microsoft.com/de2cb778-c6eb-4487-996b-87405674f603">IPropertySetStorage-Compound File Implementation</a>, you must specify STGM_SHARE_EXCLUSIVE in the <i>grfMode</i> parameter to <b>IPropertySetStorage::Open</b>. Conversely, if using the 
<a href="https://msdn.microsoft.com/0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2">IPropertySetStorage-Stand-alone Implementation</a>, <b>IPropertySetStorage::Open</b> is subject to constraints that apply to the caller-specified 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>.




## -see-also




<a href="https://msdn.microsoft.com/40dd62b8-f76a-4cd8-9a9f-6ac344389b6c">EnumAll Sample</a>



<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>



<a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a>



<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>



<a href="https://msdn.microsoft.com/c5807dd9-2928-497b-9446-729dcaeebc8a">WriteRead Sample</a>
 

 

