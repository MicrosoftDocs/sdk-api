---
UID: NF:gpmgmt.IGPMGPOCollection.get__NewEnum
title: IGPMGPOCollection::get__NewEnum
author: windows-sdk-content
description: Retrieves an enumerator for the collection.
old-location: gpmc\igpmgpocollection_get__newenum.htm
old-project: GPMC
ms.assetid: 7db1ec65-9850-4f14-b223-a7decc7648a6
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IGPMGPOCollection interface [GPMC],get__NewEnum method, IGPMGPOCollection.get__NewEnum, IGPMGPOCollection::get__NewEnum, _win32_igpmgpocollection_get__newenum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMGPOCollection interface, gpmc.igpmgpocollection_get__newenum, gpmgmt/IGPMGPOCollection::get__NewEnum
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
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMGPOCollection.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMGPOCollection::get__NewEnum


## -description


Retrieves an enumerator for the collection.


## -parameters




### -param ppIGPMGPOs [out]

Pointer to an <b>IEnumVARIANT</b> interface of an enumerator object for the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection. For more information about <b>IEnumVARIANT</b>, see the COM documentation in the Platform SDK.


## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">IGPMGPOCollection</a>
 

 

