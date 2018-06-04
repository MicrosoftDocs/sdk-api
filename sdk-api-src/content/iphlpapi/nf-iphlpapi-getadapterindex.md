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

# GetAdapterIndex function


## -description



			The 
<b>GetAdapterIndex</b> function obtains the index of an adapter, given its name.


## -parameters




### -param AdapterName [in]

A pointer to a Unicode string that specifies the name of the adapter.


### -param IfIndex [in, out]

A pointer to a <b>ULONG</b> variable that points to the index of the adapter.


## -returns




						If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.




## -remarks



Until an adapter is fully disabled, the <b>GetAdapterIndex</b> function reports the adapter as present. For example, the <a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a> function may indicate a recently disabled adapter's IP address is removed, but <b>GetAdapterIndex</b> continues to report an adapter  index until the process of disabling the adapter is complete.

When one or more adapters are present on the system, <b>GetAdapterIndex</b>  returns ERROR_DEV_NOT_EXIST when the adapter being queried does not exist. When no adapters are present, the <b>GetAdapterIndex</b> function returns ERROR_NO_DATA.

 The adapter index  may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.




## -see-also




<a href="https://msdn.microsoft.com/8cdecc84-6566-438b-86d0-3c55490a9a59">GetAdaptersInfo</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/f8035801-ca0c-4d86-bfc5-8e2d746af1b4">IP_ADAPTER_INFO</a>



<a href="_mpr_mprconfiggetfriendlyname">MprConfigGetFriendlyName</a>



<a href="_mpr_mprconfiggetguidname">MprConfigGetGuidName</a>



<a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a>
 

 

