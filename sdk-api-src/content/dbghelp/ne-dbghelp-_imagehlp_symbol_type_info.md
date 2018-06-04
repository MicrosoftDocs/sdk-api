---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _IMAGEHLP_SYMBOL_TYPE_INFO enumeration


## -description


Identifies the type of symbol information to be retrieved.


## -enum-fields




### -field TI_GET_SYMTAG

The symbol tag.

The data type is <b>DWORD*</b>.


### -field TI_GET_SYMNAME

The symbol name.

The data type is <b>WCHAR**</b>. The caller must free the buffer.


### -field TI_GET_LENGTH

The length of the type.

The data type is <b>ULONG64*</b>.


### -field TI_GET_TYPE

The type.

The data type is <b>DWORD*</b>.


### -field TI_GET_TYPEID

The type index.

The data type is <b>DWORD*</b>.


### -field TI_GET_BASETYPE

The base type for the type index.

The data type is <b>DWORD*</b>.


### -field TI_GET_ARRAYINDEXTYPEID

The type index for index of an array type.

The data type is <b>DWORD*</b>.


### -field TI_FINDCHILDREN

The type index of all children.

The data type  is a pointer to a 
<a href="https://msdn.microsoft.com/618717d2-879d-4284-a4c2-0a5102698ed9">TI_FINDCHILDREN_PARAMS</a> structure. The <b>Count</b> member should be initialized with the number of children.


### -field TI_GET_DATAKIND

The data kind.

The data type is <b>DWORD*</b>.


### -field TI_GET_ADDRESSOFFSET

The address offset.

The data type is <b>DWORD*</b>.


### -field TI_GET_OFFSET

The offset of the type in the parent. Members can use this to get their offset in a structure.

The data type is <b>DWORD*</b>.


### -field TI_GET_VALUE

The value of a constant or enumeration value.

The data type is <b>VARIANT*</b>.


### -field TI_GET_COUNT

The count of array elements.

The data type is <b>DWORD*</b>.


### -field TI_GET_CHILDRENCOUNT

The number of children.

The data type is <b>DWORD*</b>.


### -field TI_GET_BITPOSITION

The bit position of a bitfield.

The data type is <b>DWORD*</b>.


### -field TI_GET_VIRTUALBASECLASS

A value that indicates whether the base class is virtually inherited.

The data type is <b>BOOL</b>.


### -field TI_GET_VIRTUALTABLESHAPEID

The symbol interface of the type of virtual table, for a user-defined type.


### -field TI_GET_VIRTUALBASEPOINTEROFFSET

The offset of the virtual base pointer.

The data type is <b>DWORD*</b>.


### -field TI_GET_CLASSPARENTID

The type index of the class parent.

The data type is <b>DWORD*</b>.


### -field TI_GET_NESTED

A value that indicates whether the type index is nested.

The data type is <b>DWORD*</b>.


### -field TI_GET_SYMINDEX

The symbol index for a type.

The data type is <b>DWORD*</b>.


### -field TI_GET_LEXICALPARENT

The lexical parent of the type.

The data type is <b>DWORD*</b>.


### -field TI_GET_ADDRESS

The index address.

The data type is <b>ULONG64*</b>.


### -field TI_GET_THISADJUST

The offset from the <b>this</b> pointer to its actual value.

The data type is <b>DWORD*</b>.


### -field TI_GET_UDTKIND

The UDT kind.

The data type is <b>DWORD*</b>.


### -field TI_IS_EQUIV_TO

The equivalency of two types.

The data type is <b>DWORD*</b>. The value is S_OK is the two types are equivalent, and S_FALSE otherwise.


### -field TI_GET_CALLING_CONVENTION

The calling convention.

The data type is <b>DWORD</b>. The following are the valid values:


### -field TI_IS_CLOSE_EQUIV_TO

The equivalency of two symbols. This is not guaranteed to be accurate.

The data type is <b>DWORD*</b>. The value is S_OK is the two types are equivalent, and S_FALSE otherwise.


### -field TI_GTIEX_REQS_VALID

The element where the valid request bitfield should be stored.

The data type is <b>ULONG64*</b>.

This value is only used with the <a href="https://msdn.microsoft.com/77e0a8ad-8c75-4bb2-869a-670429475ccc">SymGetTypeInfoEx</a> function.


### -field TI_GET_VIRTUALBASEOFFSET

The offset in the virtual function table of a virtual function.

The data type is <b>DWORD</b>.


### -field TI_GET_VIRTUALBASEDISPINDEX

The index into the virtual base displacement table.

The data type is <b>DWORD</b>.


### -field TI_GET_IS_REFERENCE

Indicates whether a pointer type is a reference.

The data type is <b>Boolean</b>.


### -field TI_GET_INDIRECTVIRTUALBASECLASS

Indicates whether the user-defined data type is an indirect virtual base.

The data type is <b>BOOL</b>.

<b>DbgHelp 6.6 and earlier:  </b>This value is not supported.


### -field TI_GET_VIRTUALBASETABLETYPE


### -field IMAGEHLP_SYMBOL_TYPE_INFO_MAX




## -see-also




<a href="https://msdn.microsoft.com/bc94a5b1-d49d-425a-89a8-c584c3979930">SymGetTypeInfo</a>



<a href="https://msdn.microsoft.com/77e0a8ad-8c75-4bb2-869a-670429475ccc">SymGetTypeInfoEx</a>
 

 

