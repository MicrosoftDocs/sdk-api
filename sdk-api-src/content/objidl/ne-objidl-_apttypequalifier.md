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

# _APTTYPEQUALIFIER enumeration


## -description


Specifies the set of possible COM apartment type qualifiers.


## -enum-fields




### -field APTTYPEQUALIFIER_NONE

No qualifier information for the current COM apartment type is available.


### -field APTTYPEQUALIFIER_IMPLICIT_MTA

This qualifier is only valid when the <i>pAptType</i> parameter of the <a href="https://msdn.microsoft.com/ab0b6008-397f-4210-ba26-1a041b709722">CoGetApartmentType</a> function specifies APTTYPE_MTA on return. A thread has an implicit MTA apartment type if it does not initialize the COM apartment itself, and if another thread has already initialized the MTA in the process. This qualifier informs the API caller that the MTA of the thread is implicitly inherited from other threads and is not initialized directly.


### -field APTTYPEQUALIFIER_NA_ON_MTA

This qualifier is only valid when the <i>pAptType</i> parameter of the <a href="https://msdn.microsoft.com/ab0b6008-397f-4210-ba26-1a041b709722">CoGetApartmentType</a> function contains APTTYPE_NA on return. When an MTA thread creates or invokes a COM in-process object using the "Neutral" threading model, the COM apartment type of the thread switches from MTA to a Neutral apartment type. This qualifier informs the API caller that the thread has switched from the MTA apartment type to the NA type.


### -field APTTYPEQUALIFIER_NA_ON_STA

This qualifier is only valid when the <i>pAptType</i> parameter of the <a href="https://msdn.microsoft.com/ab0b6008-397f-4210-ba26-1a041b709722">CoGetApartmentType</a> function contains APTTYPE_NA on return. When an STA thread creates or invokes a COM in-process object using the "Neutral" threading model, the COM apartment type of the thread switches from STA to a Neutral apartment type. This qualifier informs the API caller that the thread has switched from the STA apartment type to the NA type.


### -field APTTYPEQUALIFIER_NA_ON_IMPLICIT_MTA

This qualifier is only valid when the <i>pAptType</i> parameter of the <a href="https://msdn.microsoft.com/ab0b6008-397f-4210-ba26-1a041b709722">CoGetApartmentType</a> function contains APTTYPE_NA on return. When an implicit MTA thread creates or invokes a COM in-process object using the "Neutral" threading model, the COM apartment type of the thread switches from the implicit MTA type to a Neutral apartment type. This qualifier informs the API caller that the thread has switched from the implicit MTA apartment type to the NA type.


### -field APTTYPEQUALIFIER_NA_ON_MAINSTA

This qualifier is only valid when the <i>pAptType</i> parameter of the <a href="https://msdn.microsoft.com/ab0b6008-397f-4210-ba26-1a041b709722">CoGetApartmentType</a> function contains APTTYPE_NA on return. When the main STA thread creates or invokes a COM in-process object using the "Neutral" threading model, the COM apartment type of the thread switches from the main STA type to a Neutral apartment type. This qualifier informs the API caller that the thread has switched from the main STA apartment type to the NA type.


### -field APTTYPEQUALIFIER_APPLICATION_STA




## -see-also




<a href="https://msdn.microsoft.com/ab0b6008-397f-4210-ba26-1a041b709722">CoGetApartmentType</a>
 

 

