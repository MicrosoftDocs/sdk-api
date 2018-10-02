---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT_OUTPUT
title: D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT_OUTPUT
author: windows-sdk-content
description: Contains the response to a D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT query.
old-location: mf\d3d11_authenticated_query_restricted_shared_resource_process_count_output.htm
tech.root: MedFound
ms.assetid: E47F560D-DF50-40A5-AEB1-A594AB9C3B07
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT_OUTPUT, D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT_OUTPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT_OUTPUT, mf.d3d11_authenticated_query_restricted_shared_resource_process_count_output
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT_OUTPUT
product: Windows
targetos: Windows
req.typenames: D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT_OUTPUT
req.redist: 
---

# D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT_OUTPUT structure


## -description


Contains the response to a <b>D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT</b> query.


## -struct-fields




### -field Output

A <a href="https://msdn.microsoft.com/D5650992-04D0-4DD2-A858-1E7FB979A9C2">D3D11_AUTHENTICATED_QUERY_OUTPUT</a> structure that contains a Message Authentication Code (MAC) and other data.


### -field RestrictedSharedResourceProcessCount

The number of processes that are allowed to open shared resources that have restricted access. A process cannot open such a resource unless the process has been granted access.




## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

