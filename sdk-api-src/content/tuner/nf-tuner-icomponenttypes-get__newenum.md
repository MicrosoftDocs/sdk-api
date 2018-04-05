---
UID: NF:tuner.IComponentTypes.get__NewEnum
title: IComponentTypes::get__NewEnum method
author: windows-driver-content
description: The get__NewEnum enumeration method supports For...Each loops in Automation clients.
old-location: mstv\icomponenttypes_get__newenum.htm
old-project: mstv
ms.assetid: 32ff7c56-3173-4aba-9884-6e388a41192d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IComponentTypes, IComponentTypes interface [Microsoft TV Technologies], get__NewEnum method, IComponentTypes::get__NewEnum, IComponentTypesget__NewEnum, get__NewEnum method [Microsoft TV Technologies], get__NewEnum method [Microsoft TV Technologies], IComponentTypes interface, get__NewEnum,IComponentTypes.get__NewEnum, mstv.icomponenttypes_get__newenum, tuner/IComponentTypes::get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IComponentTypes.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentTypes::get__NewEnum method


## -description



The <b>get__NewEnum</b> enumeration method supports <code>For...Each</code> loops in Automation clients.




## -parameters




### -param ppNewEnum [out]

Address of an interface pointer to an <b>IEnumVARIANT</b> object that will receive the new collection.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method is provided to enable scripting and Visual Basic applications to iterate through the collection in a <code>For...Each</code> loop. C++ applications should use the <a href="https://msdn.microsoft.com/c070998c-4350-4630-80c0-e3db46154845">IComponentTypes::EnumComponentTypes</a> method.

The returned <b>IEnumVARIANT</b> interface is not thread safe, because it is intended primarily for use by Automation clients. Clients should not call methods on the interface from more than one thread.




## -see-also




<a href="https://msdn.microsoft.com/47c3837b-1348-4359-ad3d-3d82c5fe3781">IComponentTypes Interface</a>
 

 

