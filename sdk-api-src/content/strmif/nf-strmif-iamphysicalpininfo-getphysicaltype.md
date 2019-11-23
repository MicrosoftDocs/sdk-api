---
UID: NF:strmif.IAMPhysicalPinInfo.GetPhysicalType
title: IAMPhysicalPinInfo::GetPhysicalType (strmif.h)

description: Note  The IAMPhysicalPinInfo interface is deprecated. Retrieves the type and name of the physical pin.
old-location: dshow\iamphysicalpininfo_getphysicaltype.htm
tech.root: DirectShow
ms.assetid: e18be591-64c7-4da0-aa28-c51dca7901b7

ms.date: 12/05/2018
ms.keywords: GetPhysicalType, GetPhysicalType method [DirectShow], GetPhysicalType method [DirectShow],IAMPhysicalPinInfo interface, IAMPhysicalPinInfo interface [DirectShow],GetPhysicalType method, IAMPhysicalPinInfo.GetPhysicalType, IAMPhysicalPinInfo::GetPhysicalType, IAMPhysicalPinInfoGetPhysicalType, dshow.iamphysicalpininfo_getphysicaltype, strmif/IAMPhysicalPinInfo::GetPhysicalType
ms.topic: method
f1_keywords: 
 - "strmif/IAMPhysicalPinInfo.GetPhysicalType"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMPhysicalPinInfo.GetPhysicalType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMPhysicalPinInfo::GetPhysicalType


## -description



<div class="alert"><b>Note</b>  The <code>IAMPhysicalPinInfo</code> interface is deprecated.</div>
<div> </div>
Retrieves the type and name of the physical pin.




## -parameters




### -param pType [out]

Pointer to a variable that receives a value indicating the pin's type. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-physicalconnectortype">PhysicalConnectorType</a> enumeration defines the pin type values.


### -param ppszType [out]

Address of a pointer to a buffer that receives a human-readable string identifying the pin type.


## -returns



Returns S_OK if a valid physical pin value is found. Otherwise, returns VFW_E_NO_ACCEPTABLE_TYPES.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamphysicalpininfo">IAMPhysicalPinInfo Interface</a>
 

 

