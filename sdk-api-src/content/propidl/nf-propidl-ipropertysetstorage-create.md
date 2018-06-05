---
UID: NF:propidl.IPropertySetStorage.Create
title: IPropertySetStorage::Create
author: windows-sdk-content
description: Creates and opens a new property set in the property set storage object.
old-location: stg\ipropertysetstorage_create.htm
old-project: Stg
ms.assetid: 9307788d-bce6-4025-8043-8b68e874a62b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: Create, Create method [Structured Storage], Create method [Structured Storage],IPropertySetStorage interface, IPropertySetStorage interface [Structured Storage],Create method, IPropertySetStorage.Create, IPropertySetStorage::Create, _stg_ipropertysetstorage_create, propidl/IPropertySetStorage::Create, stg.ipropertysetstorage_create
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
-	IPropertySetStorage.Create
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPropertySetStorage::Create


## -description


The <b>Create</b> method 
			creates and opens a new property set in the property set storage object.


## -parameters




### -param rfmtid




### -param pclsid [in]

A pointer to the initial class identifier CLSID for this property set. May be <b>NULL</b>, in which case it is set to all zeroes. The CLSID is the CLSID of a class that displays and/or provides programmatic access to the property values. If there is no such class, it is recommended that the FMTID be used.


### -param grfFlags [in]

The values from <a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>.


### -param grfMode [in]

An access mode in which the newly created property set is to be opened, taken from certain values of <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM_Constants</a>, as described in the following Remarks section.


### -param ppprstg






#### - fmtid [in]

The FMTID of the property set to be created. For information about FMTIDs that are well-known and predefined in the Platform SDK, see 
<a href="https://msdn.microsoft.com/cc99ce1b-beb5-4340-91ed-3aed5bdad2bd">Predefined Property Set Format Identifiers</a>.


#### - ppProgStg [out]

A pointer to the output variable that receives the <a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface pointer.


## -returns




						This method supports the standard return value E_UNEXPECTED, as well as the following:




## -remarks



<b>IPropertySetStorage::Create</b> creates and opens a new property set subobject (supporting the 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface) contained in this property set storage object. The property set automatically contains code page and locale ID properties. These are set to the Unicode and the current user default, respectively.

The <i>grfFlags</i> parameter is a combination of values taken from <a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>. If the PROPSETFLAG_ANSI value from this enumeration is used, the code page is set to the current system default, rather than Unicode.

The <i>grfMode</i> parameter specifies the access mode in which the newly created set is to be opened. Values for this parameter are as in the <i>grfMode</i> parameter to 
<a href="https://msdn.microsoft.com/a0e2239f-b908-460a-98e8-c805c1d84def">IPropertySetStorage::Open</a>, with the addition of the values listed in the following table.

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
<a href="https://msdn.microsoft.com/d0ca649a-d405-4c34-af02-9c2ca8b2790e">Storage and Stream Objects for a Property Set</a>.

This method is subject to the constraints of the underlying <a href="https://msdn.microsoft.com/168f5ac9-8a72-4356-82a4-de3a7ec72c05">IStorage::CreateStream</a> (for simple property sets) or <a href="https://msdn.microsoft.com/8c74cacf-8d3c-4d57-b1e9-dc5e4f281717">IStorage::CreateStorage</a> (for nonsimple property sets). For example, when using the 
<a href="https://msdn.microsoft.com/de2cb778-c6eb-4487-996b-87405674f603">IPropertySetStorage-Compound File Implementation</a>, specify STGM_SHARE_EXCLUSIVE in the <i>grfMode</i> parameter to <b>IPropertySetStorage::Create</b>. Conversely, if  using the 
<a href="https://msdn.microsoft.com/0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2">IPropertySetStorage-Stand-alone Implementation</a>, <b>IPropertySetStorage::Create</b> is subject to constraints that apply to the caller-specified 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>.




## -see-also




<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>



<a href="https://msdn.microsoft.com/a0e2239f-b908-460a-98e8-c805c1d84def">IPropertySetStorage::Open</a>



<a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>



<a href="https://msdn.microsoft.com/f0d0664a-2cfd-4eb0-b1d5-47d1545394fd">StgCreatePropSetStg Sample</a>



<a href="https://msdn.microsoft.com/c5807dd9-2928-497b-9446-729dcaeebc8a">WriteRead Sample</a>
 

 

