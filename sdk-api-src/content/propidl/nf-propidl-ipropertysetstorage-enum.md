---
UID: NF:propidl.IPropertySetStorage.Enum
title: IPropertySetStorage::Enum
author: windows-sdk-content
description: The Enum method creates an enumerator object which contains information on the property sets stored in this property set storage. On return, this method supplies a pointer to the IEnumSTATPROPSETSTG pointer on the enumerator object.
old-location: stg\ipropertysetstorage_enum.htm
old-project: Stg
ms.assetid: 979ee86b-fabc-428c-8134-f16c2a33270f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Enum, Enum method [Structured Storage], Enum method [Structured Storage],IPropertySetStorage interface, IPropertySetStorage [Strctd Stg],Enum, IPropertySetStorage interface [Structured Storage],Enum method, IPropertySetStorage.Enum, IPropertySetStorage::Enum, _stg_ipropertysetstorage_enum, propidl/IPropertySetStorage::Enum, stg.ipropertysetstorage_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propidl.h
req.include-header: Objbase.h
req.redist: 
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
tech.root: 
req.typenames: PROFILEINFOW, *LPPROFILEINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IPropertySetStorage.Enum
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IPropertySetStorage::Enum


## -description


The <b>Enum</b> method creates an enumerator object which contains information on the property sets stored in this property set storage. On return, this method supplies a pointer to the 
<a href="https://msdn.microsoft.com/8d5e658f-312c-4c91-8794-808b2e8dd182">IEnumSTATPROPSETSTG</a> pointer on the enumerator object.


## -parameters




### -param ppenum [out]

Pointer to 
<a href="https://msdn.microsoft.com/8d5e658f-312c-4c91-8794-808b2e8dd182">IEnumSTATPROPSETSTG</a> pointer variable that receives the interface pointer to the newly created enumerator object.


## -returns



This method can return one of these values.




## -remarks



<b>IPropertySetStorage::Enum</b> creates an enumerator object that can be used to iterate through 
<a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structures. These sometimes provide information on the property sets managed by 
<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>. This method, on return, supplies a pointer to the 
<a href="https://msdn.microsoft.com/8d5e658f-312c-4c91-8794-808b2e8dd182">IEnumSTATPROPSETSTG</a> interface on this enumerator object on return.




## -see-also




<a href="https://msdn.microsoft.com/40dd62b8-f76a-4cd8-9a9f-6ac344389b6c">EnumAll Sample</a>



<a href="https://msdn.microsoft.com/8d5e658f-312c-4c91-8794-808b2e8dd182">IEnumSTATPROPSETSTG</a>



<a href="https://msdn.microsoft.com/1ce36e40-518c-411b-be5a-835a2dd0995e">IEnumSTATPROPSETSTG - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>
 

 

