---
UID: NF:iphlpapi.GetAdapterIndex
title: GetAdapterIndex function (iphlpapi.h)
author: windows-sdk-content
description: The GetAdapterIndex function obtains the index of an adapter, given its name.
old-location: iphlp\getadapterindex.htm
tech.root: IpHlp
ms.assetid: e98ee6b3-30c2-4629-859e-e7440781cd86
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAdapterIndex, GetAdapterIndex function [IP Helper], _iphlp_getadapterindex, iphlp.getadapterindex, iphlpapi/GetAdapterIndex
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetAdapterIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



<a href="https://msdn.microsoft.com/en-us/library/Aa375858(v=VS.85).aspx">MprConfigGetFriendlyName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375859(v=VS.85).aspx">MprConfigGetGuidName</a>



<a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a>
 

 

