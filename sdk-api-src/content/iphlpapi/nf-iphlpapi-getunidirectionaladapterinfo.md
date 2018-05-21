---
UID: NF:iphlpapi.GetUniDirectionalAdapterInfo
title: GetUniDirectionalAdapterInfo function
author: windows-driver-content
description: The GetUniDirectionalAdapterInfo function retrieves information about the unidirectional adapters installed on the local computer. A unidirectional adapter is an adapter that can receive datagrams, but not transmit them.
old-location: iphlp\getunidirectionaladapterinfo.htm
old-project: IpHlp
ms.assetid: 32aa3a8e-ae74-4da9-bc8d-b28e270d9702
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetUniDirectionalAdapterInfo, GetUniDirectionalAdapterInfo function [IP Helper], _iphlp_getunidirectionaladapterinfo, iphlp.getunidirectionaladapterinfo, iphlpapi/GetUniDirectionalAdapterInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
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
req.typenames: NET_ADDRESS_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	GetUniDirectionalAdapterInfo
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetUniDirectionalAdapterInfo function


## -description


The 
<b>GetUniDirectionalAdapterInfo</b> function retrieves information about the unidirectional adapters installed on the local computer. A unidirectional adapter is an adapter that can receive datagrams, but not transmit them.


## -parameters




### -param pIPIfInfo [out]

Pointer to an 
<a href="https://msdn.microsoft.com/225b93ae-e34f-4e5b-a699-1fdd342265c6">IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</a> structure that receives information about the unidirectional adapters installed on the local computer.


### -param dwOutBufLen [out]

Pointer to a <b>ULONG</b> variable that receives the size of the structure pointed to by the <i>pIPIfInfo</i> parameter.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.




## -see-also




<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/225b93ae-e34f-4e5b-a699-1fdd342265c6">IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</a>
 

 

