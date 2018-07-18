---
UID: NE:objidl._APTTYPEQUALIFIER
title: "_APTTYPEQUALIFIER"
author: windows-sdk-content
description: Specifies the set of possible COM apartment type qualifiers.
old-location: com\apttypequalifier.htm
old-project: com
ms.assetid: ac28076d-d266-4939-b6c1-d56494ffbcd8
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: APTTYPEQUALIFIER, APTTYPEQUALIFIER enumeration [COM], APTTYPEQUALIFIER_IMPLICIT_MTA, APTTYPEQUALIFIER_NA_ON_IMPLICIT_MTA, APTTYPEQUALIFIER_NA_ON_MAINSTA, APTTYPEQUALIFIER_NA_ON_MTA, APTTYPEQUALIFIER_NA_ON_STA, APTTYPEQUALIFIER_NONE, _APTTYPEQUALIFIER, com.apttypequalifier, objidlbase/APTTYPEQUALIFIER, objidlbase/APTTYPEQUALIFIER_IMPLICIT_MTA, objidlbase/APTTYPEQUALIFIER_NA_ON_IMPLICIT_MTA, objidlbase/APTTYPEQUALIFIER_NA_ON_MAINSTA, objidlbase/APTTYPEQUALIFIER_NA_ON_MTA, objidlbase/APTTYPEQUALIFIER_NA_ON_STA, objidlbase/APTTYPEQUALIFIER_NONE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidl.h
req.include-header: Objidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: APTTYPEQUALIFIER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - APTTYPEQUALIFIER
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: ADAM
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


### -field APTTYPEQUALIFIER_RESERVED_1




## -see-also




<a href="https://msdn.microsoft.com/ab0b6008-397f-4210-ba26-1a041b709722">CoGetApartmentType</a>
 

 

