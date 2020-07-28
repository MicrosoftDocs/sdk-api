---
UID: NF:propidl.IPropertyStorage.Enum
title: IPropertyStorage::Enum (propidl.h)
description: The Enum method creates an enumerator object designed to enumerate data of type STATPROPSTG, which contains information on the current property set. On return, this method supplies a pointer to the IEnumSTATPROPSTG pointer on this object.
helpviewer_keywords: ["Enum","Enum method [Structured Storage]","Enum method [Structured Storage]","IPropertyStorage interface","IPropertyStorage [Strctd Stg]","Enum","IPropertyStorage interface [Structured Storage]","Enum method","IPropertyStorage.Enum","IPropertyStorage::Enum","_stg_ipropertystorage_enum","propidl/IPropertyStorage::Enum","stg.ipropertystorage_enum"]
old-location: stg\ipropertystorage_enum.htm
tech.root: Stg
ms.assetid: 73f834cf-b6e4-4a48-bbdc-0c4ba87aacaf
ms.date: 12/05/2018
ms.keywords: Enum, Enum method [Structured Storage], Enum method [Structured Storage],IPropertyStorage interface, IPropertyStorage [Strctd Stg],Enum, IPropertyStorage interface [Structured Storage],Enum method, IPropertyStorage.Enum, IPropertyStorage::Enum, _stg_ipropertystorage_enum, propidl/IPropertyStorage::Enum, stg.ipropertystorage_enum
f1_keywords:
- propidl/IPropertyStorage.Enum
dev_langs:
- c++
req.header: propidl.h
req.include-header: Objbase.h, Propidlbase.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyStorage::Enum


## -description


The <b>Enum</b> method creates an enumerator object designed to enumerate data of type 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropstg">STATPROPSTG</a>, which contains information on the current property set. On return, this method supplies a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ienumstatpropstg">IEnumSTATPROPSTG</a> pointer on this object.


## -parameters




### -param ppenum [out]

Pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ienumstatpropstg">IEnumSTATPROPSTG</a> pointer variable that receives the interface pointer to the new enumerator object.


## -returns



This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



<b>IPropertyStorage::Enum</b> creates an enumeration object that can be used to iterate 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropstg">STATPROPSTG</a> structures. On return, this method supplies a pointer to an instance of the 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ienumstatpropstg">IEnumSTATPROPSTG</a> interface on this object, whose methods you can call to obtain information about the current property set.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/enumall-sample">EnumAll Sample</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ienumstatpropstg">IEnumSTATPROPSTG</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/ienumstatpropstg-compound-file-implementation">IEnumSTATPROPSTG - Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/samples">Samples</a>
 

 

