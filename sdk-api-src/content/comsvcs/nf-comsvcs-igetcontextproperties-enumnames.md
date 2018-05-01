---
UID: NF:comsvcs.IGetContextProperties.EnumNames
title: IGetContextProperties::EnumNames method
author: windows-driver-content
description: Retrieves a list of the names of the current context properties.
old-location: cos\igetcontextproperties_enumnames.htm
old-project: cossdk
ms.assetid: 01ff9650-f7f1-440c-88d2-75ba793a2396
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: EnumNames method [COM+], EnumNames method [COM+], IGetContextProperties interface, EnumNames,IGetContextProperties.EnumNames, IGetContextProperties, IGetContextProperties interface [COM+], EnumNames method, IGetContextProperties::EnumNames, _cos_IGetContextProperties_EnumNames, comsvcs/IGetContextProperties::EnumNames, cos.igetcontextproperties_enumnames
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
-	IGetContextProperties.EnumNames
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetContextProperties::EnumNames method


## -description


Retrieves a list of the names of the current context properties.


## -parameters




### -param ppenum [out, retval]

An <a href="https://msdn.microsoft.com/9f70b554-3cdd-4a4b-b180-c6de6182a46a">IEnumNames</a> interface providing access to a list of the names of the current context properties.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/5e960c75-b074-4d4b-b5d6-252c26c70176">IGetContextProperties</a>
 

 

