---
UID: NC:stm.PGET_FIRST_ORDERED_SERVICE
title: PGET_FIRST_ORDERED_SERVICE
author: windows-sdk-content
description: The GetFirstOrderedService function returns the first service in the specified order from the designated subset of services in the table.
old-location: rras\getfirstorderedservice.htm
old-project: rras
ms.assetid: 193ca671-3b1a-493f-a655-a27f6348f5d2
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetFirstOrderedService, GetFirstOrderedService callback function [RAS], PGET_FIRST_ORDERED_SERVICE, PGET_FIRST_ORDERED_SERVICE callback, STM_ORDER_BY_INTERFACE_TYPE_NAME, STM_ORDER_BY_TYPE_AND_NAME, _mpr_getfirstorderedservice, rras.getfirstorderedservice, stm/GetFirstOrderedService
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
tech.root: 
req.typenames: SEC_WINNT_CREDUI_CONTEXT_VECTOR, *PSEC_WINNT_CREDUI_CONTEXT_VECTOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Stm.h
api_name:
 - GetFirstOrderedService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# PGET_FIRST_ORDERED_SERVICE callback function


## -description


The 
<b>GetFirstOrderedService</b> function returns the first service in the specified order from the designated subset of services in the table.


## -parameters




### -param OrderingMethod [in]

Specifies the order in which the services are searched. This parameter must be one of the following values. 


					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STM_ORDER_BY_TYPE_AND_NAME"></a><a id="stm_order_by_type_and_name"></a><dl>
<dt><b>STM_ORDER_BY_TYPE_AND_NAME</b></dt>
</dl>
</td>
<td width="60%">
Search the services first by type and then by name.

</td>
</tr>
<tr>
<td width="40%"><a id="STM_ORDER_BY_INTERFACE_TYPE_NAME"></a><a id="stm_order_by_interface_type_name"></a><dl>
<dt><b>STM_ORDER_BY_INTERFACE_TYPE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Search the services first by interface index, then by type, and finally by name.

</td>
</tr>
</table>
 


### -param ExclusionFlags [in]

Specifies the limits the set of examined services to a subset defined by <i>ExclusionFlags</i> and the values in the members of the structure pointed to by the <i>Service</i> parameter. See 
<a href="https://msdn.microsoft.com/68ed5662-ffa8-456b-b79c-a6fb27339262">CreateServiceEnumerationHandle</a> for a description of the possible flags.


### -param Service [in, out]

Pointer to an 
<a href="https://msdn.microsoft.com/37da1071-b665-405c-a4ce-f1a484aeb19b">IPX_SERVICE</a> structure. 




On input, the values in the members correspond to flags specified in <i>ExclusionFlags</i>.

On output, the first service that matches specified criteria.


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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
Services that match the specified criteria do not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/68ed5662-ffa8-456b-b79c-a6fb27339262">CreateServiceEnumerationHandle</a>



<a href="https://msdn.microsoft.com/e93e3bf2-80a2-44ec-a067-58220cdd31b4">IPX Service Table Management</a>



<a href="https://msdn.microsoft.com/37da1071-b665-405c-a4ce-f1a484aeb19b">IPX_SERVICE</a>



<a href="https://msdn.microsoft.com/eb31f1ad-5761-4112-8c05-51a627b9e0b7">Service Table Management Functions</a>
 

 

