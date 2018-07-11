---
UID: NF:strmif.IAMPhysicalPinInfo.GetPhysicalType
title: IAMPhysicalPinInfo::GetPhysicalType
author: windows-sdk-content
description: Note  The IAMPhysicalPinInfo interface is deprecated. Retrieves the type and name of the physical pin.
old-location: dshow\iamphysicalpininfo_getphysicaltype.htm
old-project: DirectShow
ms.assetid: e18be591-64c7-4da0-aa28-c51dca7901b7
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetPhysicalType, GetPhysicalType method [DirectShow], GetPhysicalType method [DirectShow],IAMPhysicalPinInfo interface, IAMPhysicalPinInfo interface [DirectShow],GetPhysicalType method, IAMPhysicalPinInfo.GetPhysicalType, IAMPhysicalPinInfo::GetPhysicalType, IAMPhysicalPinInfoGetPhysicalType, dshow.iamphysicalpininfo_getphysicaltype, strmif/IAMPhysicalPinInfo::GetPhysicalType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMPhysicalPinInfo.GetPhysicalType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMPhysicalPinInfo::GetPhysicalType


## -description



<div class="alert"><b>Note</b>  The <code>IAMPhysicalPinInfo</code> interface is deprecated.</div>
<div> </div>
Retrieves the type and name of the physical pin.




## -parameters




### -param pType [out]

Pointer to a variable that receives a value indicating the pin's type. The <a href="https://msdn.microsoft.com/00635c01-f068-43b0-b7b6-d26f27886f71">PhysicalConnectorType</a> enumeration defines the pin type values.


### -param ppszType [out]

Address of a pointer to a buffer that receives a human-readable string identifying the pin type.


## -returns



Returns S_OK if a valid physical pin value is found. Otherwise, returns VFW_E_NO_ACCEPTABLE_TYPES.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d1d05d2c-018e-421f-bfb9-810d708f726c">IAMPhysicalPinInfo Interface</a>
 

 

