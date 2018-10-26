---
UID: NC:stm.PGET_NEXT_ORDERED_SERVICE
title: PGET_NEXT_ORDERED_SERVICE
author: windows-sdk-content
description: The GetNextOrderedService function returns the next service from a subset of services in the table. The service returned is the next service after a given input service using the ordering method specified.
old-location: rras\getnextorderedservice.htm
tech.root: rras
ms.assetid: e25d7086-cfb7-41ea-8f4e-7e4f065830d9
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetNextOrderedService, GetNextOrderedService callback function [RAS], PGET_NEXT_ORDERED_SERVICE, PGET_NEXT_ORDERED_SERVICE callback, _mpr_getnextorderedservice, rras.getnextorderedservice, stm/GetNextOrderedService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: stm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Stm.h
api_name:
 - GetNextOrderedService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PGET_NEXT_ORDERED_SERVICE callback function


## -description


The 
<b>GetNextOrderedService</b> function returns the next service from a subset of services in the table. The service returned is the next service after a given input service using the ordering method specified.


## -parameters




### -param OrderingMethod [in]

Specifies the order in which the services are searched. See 
<a href="https://msdn.microsoft.com/193ca671-3b1a-493f-a655-a27f6348f5d2">GetFirstOrderedService</a> for a description of the various ordering methods.


### -param ExclusionFlags [in]

Limits the set of examined services to a subset defined by <i>ExclusionFlags</i> and the values in the corresponding members of the structure pointed to by the <i>Service</i> parameter. See 
<a href="https://msdn.microsoft.com/68ed5662-ffa8-456b-b79c-a6fb27339262">CreateServiceEnumerationHandle</a> for a description of the possible flags.


### -param Service [in, out]

Pointer to an 
<a href="https://msdn.microsoft.com/37da1071-b665-405c-a4ce-f1a484aeb19b">IPX_SERVICE</a> structure. 




On input, specifies the service from which to continue searching; also contains member values that correspond to the specified <i>ExclusionFlags</i>.

On output, the structure contains the first service that follows the input service and matches the specified criteria.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_SERVICES</b></dt>
</dl>
</td>
<td width="60%">
There are no more services matching the specified criteria.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the  parameters is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/68ed5662-ffa8-456b-b79c-a6fb27339262">CreateServiceEnumerationHandle</a>



<a href="https://msdn.microsoft.com/e93e3bf2-80a2-44ec-a067-58220cdd31b4">IPX Service Table Management</a>



<a href="https://msdn.microsoft.com/37da1071-b665-405c-a4ce-f1a484aeb19b">IPX_SERVICE</a>



<a href="https://msdn.microsoft.com/eb31f1ad-5761-4112-8c05-51a627b9e0b7">Service Table Management Functions</a>
 

 

