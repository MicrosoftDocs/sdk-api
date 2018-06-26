---
UID: NF:objidl.IStorage.EnumElements
title: IStorage::EnumElements
author: windows-sdk-content
description: The EnumElements method retrieves a pointer to an enumerator object that can be used to enumerate the storage and stream objects contained within this storage object.
old-location: stg\istorage_enumelements.htm
old-project: Stg
ms.assetid: 29ca157e-40e2-4e9a-95fb-a31bb45570f2
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: EnumElements, EnumElements method [Structured Storage], EnumElements method [Structured Storage],IStorage interface, IStorage interface [Structured Storage],EnumElements method, IStorage.EnumElements, IStorage::EnumElements, _stg_istorage_enumelements, objidl/IStorage::EnumElements, stg.istorage_enumelements
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage.EnumElements
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IStorage::EnumElements


## -description



			The <b>EnumElements</b> method retrieves a pointer to an enumerator object that can be used to enumerate the storage and stream objects contained within this storage object.


## -parameters




### -param reserved1 [in]

Reserved for future use; must be zero.


### -param reserved2 [in]

Reserved for future use; must be <b>NULL</b>.


### -param reserved3 [in]

Reserved for future use; must be zero.


### -param ppenum [out]

Pointer to 
<a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a>* pointer variable that receives the interface pointer to the new enumerator object.


## -returns



This method can return one of these values.




## -remarks



The enumerator object returned by this method implements the 
<a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a> interface, one of the standard enumerator interfaces that contain the <b>Next</b>, <b>Reset</b>, 
<b>Clone</b>, and <b>Skip</b> methods. 
<b>IEnumSTATSTG</b> enumerates the data stored in an array of 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures.

The storage object must be open in read mode to allow the enumeration of its elements.

The order in which the elements are enumerated and whether the enumerator is a snapshot or always reflects the current state of the storage object, and depends on the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> implementation.




## -see-also




<a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a>



<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a>
 

 

