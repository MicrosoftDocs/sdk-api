---
UID: NF:propidl.IPropertyStorage.Enum
title: IPropertyStorage::Enum
author: windows-sdk-content
description: The Enum method creates an enumerator object designed to enumerate data of type STATPROPSTG, which contains information on the current property set. On return, this method supplies a pointer to the IEnumSTATPROPSTG pointer on this object.
old-location: stg\ipropertystorage_enum.htm
tech.root: Stg
ms.assetid: 73f834cf-b6e4-4a48-bbdc-0c4ba87aacaf
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Enum, Enum method [Structured Storage], Enum method [Structured Storage],IPropertyStorage interface, IPropertyStorage [Strctd Stg],Enum, IPropertyStorage interface [Structured Storage],Enum method, IPropertyStorage.Enum, IPropertyStorage::Enum, _stg_ipropertystorage_enum, propidl/IPropertyStorage::Enum, stg.ipropertystorage_enum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IPropertyStorage.Enum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyStorage::Enum


## -description


The <b>Enum</b> method creates an enumerator object designed to enumerate data of type 
<a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a>, which contains information on the current property set. On return, this method supplies a pointer to the 
<a href="https://msdn.microsoft.com/e625e52a-5628-4d18-9282-aa1c141c83af">IEnumSTATPROPSTG</a> pointer on this object.


## -parameters




### -param ppenum [out]

Pointer to 
<a href="https://msdn.microsoft.com/e625e52a-5628-4d18-9282-aa1c141c83af">IEnumSTATPROPSTG</a> pointer variable that receives the interface pointer to the new enumerator object.


## -returns



This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



<b>IPropertyStorage::Enum</b> creates an enumeration object that can be used to iterate 
<a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures. On return, this method supplies a pointer to an instance of the 
<a href="https://msdn.microsoft.com/e625e52a-5628-4d18-9282-aa1c141c83af">IEnumSTATPROPSTG</a> interface on this object, whose methods you can call to obtain information about the current property set.




## -see-also




<a href="https://msdn.microsoft.com/40dd62b8-f76a-4cd8-9a9f-6ac344389b6c">EnumAll Sample</a>



<a href="https://msdn.microsoft.com/e625e52a-5628-4d18-9282-aa1c141c83af">IEnumSTATPROPSTG</a>



<a href="https://msdn.microsoft.com/8fa536f4-cce6-47e4-a860-2f43e48fa469">IEnumSTATPROPSTG - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>
 

 

