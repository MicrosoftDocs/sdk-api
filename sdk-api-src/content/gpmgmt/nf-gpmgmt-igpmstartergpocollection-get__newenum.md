---
UID: NF:gpmgmt.IGPMStarterGPOCollection.get__NewEnum
title: IGPMStarterGPOCollection::get__NewEnum
author: windows-sdk-content
description: Retrieves an enumerator for the collection.
old-location: gpmc\igpmstartergpocollection_get__newenum.htm
old-project: GPMC
ms.assetid: 0e0e6360-46a9-49ff-9eb9-0ea708258ebb
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IGPMStarterGPOCollection interface [GPMC],get__NewEnum method, IGPMStarterGPOCollection.get__NewEnum, IGPMStarterGPOCollection::get__NewEnum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMStarterGPOCollection interface, gpmc.igpmstartergpocollection_get__newenum, gpmgmt/IGPMStarterGPOCollection::get__NewEnum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMStarterGPOCollection.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMStarterGPOCollection::get__NewEnum


## -description


Retrieves an enumerator for the collection.


## -parameters




### -param ppIGPMTemplates [out]

Pointer to an <b>IEnumVARIANT</b> interface of an enumerator object for the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection. For more information about <b>IEnumVARIANT</b>, see the COM documentation in the Platform SDK.


## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain2</a>



<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">IGPMStarterGPO</a>



<a href="https://msdn.microsoft.com/b650b1c6-0597-468a-afdc-a21d61f1a8a0">IGPMStarterGPOCollection</a>
 

 

