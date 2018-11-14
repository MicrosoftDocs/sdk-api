---
UID: NF:gpmgmt.IGPMSOMCollection.get__NewEnum
title: IGPMSOMCollection::get__NewEnum
author: windows-sdk-content
description: Retrieves an enumerator for the collection.
old-location: gpmc\igpmsomcollection_get__newenum.htm
tech.root: GPMC
ms.assetid: 3e6a33d8-5435-4ae9-93e7-439441d0f098
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IGPMSOMCollection interface [GPMC],get__NewEnum method, IGPMSOMCollection.get__NewEnum, IGPMSOMCollection::get__NewEnum, _win32_igpmsomcollection_get__newenum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMSOMCollection interface, gpmc.igpmsomcollection_get__newenum, gpmgmt/IGPMSOMCollection::get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMSOMCollection.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gpmgmt.h
: 
- IGPMSOMCollection.get__NewEnum
: 
---

# IGPMSOMCollection::get__NewEnum


## -description


Retrieves an enumerator for the collection.


## -parameters




### -param ppIGPMSOM [out]

Pointer to an <b>IEnumVARIANT</b> interface of an enumerator object for the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection. For more information about <b>IEnumVARIANT</b>, see the COM documentation in the Platform SDK.


## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">IGPMSOM</a>



<a href="https://msdn.microsoft.com/079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d">IGPMSOMCollection</a>
 

 

