---
UID: NF:comsvcs.IContextProperties.EnumNames
title: IContextProperties::EnumNames method
author: windows-driver-content
description: Retrieves a reference to an enumerator for the context object properties.
old-location: cos\icontextproperties_enumnames.htm
old-project: cossdk
ms.assetid: cae9eaf7-a422-4daa-9f0a-e7863f167112
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: EnumNames method [COM+], EnumNames method [COM+], IContextProperties interface, EnumNames,IContextProperties.EnumNames, IContextProperties, IContextProperties interface [COM+], EnumNames method, IContextProperties::EnumNames, _cos_IContextProperties_EnumNames, comsvcs/IContextProperties::EnumNames, cos.icontextproperties_enumnames
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IContextProperties.EnumNames
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IContextProperties::EnumNames method


## -description


Retrieves a reference to an enumerator for the context object properties.


## -parameters




### -param ppenum [out]

A reference to the <a href="https://msdn.microsoft.com/9f70b554-3cdd-4a4b-b180-c6de6182a46a">IEnumNames</a> interface on a new enumerator object that you can use to iterate through all the context object properties.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



Use the <b>EnumNames</b> method to obtain a reference to an enumerator object. The returned <a href="https://msdn.microsoft.com/9f70b554-3cdd-4a4b-b180-c6de6182a46a">IEnumNames</a> interface exposes several methods you can use to iterate through a list of <b>BSTR</b> values representing context object properties. When you have a name, you can use the <a href="https://msdn.microsoft.com/dc7748b4-5cf4-41c6-af7d-82b2478b084c">GetProperty</a> method to obtain a reference to the context object property it represents. As with any COM object, you must release an enumerator object when you are finished using it.




## -see-also




<a href="https://msdn.microsoft.com/95a5cfda-7587-496e-ba16-0dd2e8a4db32">IContextProperties</a>
 

 

