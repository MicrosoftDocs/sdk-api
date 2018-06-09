---
UID: NS:roparameterizediid.IRoSimpleMetaDataBuilder
title: IRoSimpleMetaDataBuilder
author: windows-sdk-content
description: Provides a metadata locator with a destination for the metadata it has discovered.
old-location: winrt\irosimplemetadatabuilder_struct.htm
old-project: WinRT
ms.assetid: 031B9F9B-FF77-4524-87B7-D786459569C3
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IRoSimpleMetaDataBuilder, IRoSimpleMetaDataBuilder structure [Windows Runtime], roparameterizediid/IRoSimpleMetaDataBuilder, winrt.irosimplemetadatabuilder_struct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: roparameterizediid.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - roparameterizediid.h
api_name:
 - IRoSimpleMetaDataBuilder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRoSimpleMetaDataBuilder structure


## -description


Provides a metadata locator with a destination for the metadata it has discovered.

This member supports the Windows Runtime infrastructure and is not intended to be used directly from your code.


## -struct-fields






#### - SetDelegate

Assigns a delegate to the metadata builder.



#### iid

COM interface IID for the specified delegate type.


#### - SetEnum

Assigns an enumeration to the metadata builder.

The <i>baseType</i> of plain enumerations defaults to <b>Int32</b>. The <i>baseType</i> of flags enumerations defaults to <b>UInt32</b>.



#### name

The fully qualified name of the specified enumeration type.



#### baseType

The base type of the enumeration, as specified by the metadata. 


#### - SetInterfaceGroupParameterizedDefault

Assigns an interface group with a parameterized interface as the default interface  to the metadata builder.

Call this method when an interface group has a parameterized interface as its default interface.                           



#### name

The fully qualified name of the specified interface group type.



#### elementCount

The number of elements in the <i>defaultInterfaceNameElements</i> array.



#### defaultInterfaceNameElements

An array, as would be returned by <a href="https://msdn.microsoft.com/AF007D43-7BAC-4753-9D2B-8F397B4A464A">RoParseTypeName</a>, that specifies a parameterized type instance.


#### - SetInterfaceGroupSimpleDefault

Assigns an interface group to the metadata builder.





#### name

The fully qualified name of the specified interface group type.



#### defaultInterfaceName

The fully qualified name of the default interface (must be a non-parametric type).



#### defaultInterfaceIID

Optional. 
If null, a separate call will be made to resolve the default interface type.
If not null, pointer to a GUID that contains the IID for the default interface named by <i>defaultInterfaceName</i>.



#### - SetParameterizedDelegate

Assigns a parameterized delegate to the metadata builder.

This method is only for the non-instantiated parameterized interface. Instances are handled by <a href="https://msdn.microsoft.com/DE908C82-5D7C-415C-B08B-31786589979B">RoGetParameterizedTypeInstanceIID</a>, and the caller does not need to parse them.



#### piid

The IID of the specified parameterized delegate type.



#### numArgs

The number of type arguments required by the specified parameterized delegate type.


#### - SetParameterizedInterface

Assigns a parameterized interface to the metadata builder.

This method is only for the non-instantiated parameterized interface. Instances are handled by <a href="https://msdn.microsoft.com/DE908C82-5D7C-415C-B08B-31786589979B">RoGetParameterizedTypeInstanceIID</a>, and the caller does not need to parse them. 



#### piid

The IID of the specified parameterized interface type.



#### numArgs

The number of type arguments required by the specified parameterized interface type.


#### - SetRuntimeClassParameterizedDefault

Assigns a parameterized run-time class to the metadata builder.



#### name

The fully qualified name of the specified run-time class type.



#### elementCount

The number of elements in the <i>defaultInterfaceNameElements</i> array.



#### defaultInterfaceNameElements

An array, as would be returned by <a href="https://msdn.microsoft.com/AF007D43-7BAC-4753-9D2B-8F397B4A464A">RoParseTypeName</a>, that specified a parameterized type instance.


#### - SetRuntimeClassSimpleDefault

Assigns a run-time class to the metadata builder.



#### name

The fully qualified name of the specified run-time class type.



#### defaultInterfaceName

The fully qualified name of the default interface (must be a non-parametric type).



#### defaultInterfaceIID

Optional. 
If null, a separate call will be made to resolve the default interface type.
If not null, pointer to a GUID that contains the IID for the default interface named by <i>defaultInterfaceName</i>.



#### - SetStruct

Assigns a structure to the metadata builder.



#### name

The fully qualified name of the specified structure type.



#### numFields

The number of fields in the structure, specifying the length of the <i>fieldTypeNames</i> array.



#### fieldTypeNames

An array of strings specifying the types of each field in the structure, in the order that they appear in metadata. This order matches layout order in memory.


#### - SetWinRtInterface

Assigns a Windows Runtime interface to the metadata builder.


<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> and other non-Windows Runtime interfaces are not allowed. Not for use with parameterized type instances.



#### iid

The IID for the interface.

