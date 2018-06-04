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



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>
 

 

