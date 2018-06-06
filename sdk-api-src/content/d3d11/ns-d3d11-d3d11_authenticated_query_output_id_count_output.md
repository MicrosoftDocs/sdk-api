---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_OUTPUT
title: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_OUTPUT
author: windows-sdk-content
description: Contains the response to a D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT query.
old-location: mf\d3d11_authenticated_query_output_id_count_output.htm
old-project: medfound
ms.assetid: DDA18765-A086-40CE-8502-3A48B29DFCB6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_OUTPUT, D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_OUTPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_OUTPUT, mf.d3d11_authenticated_query_output_id_count_output
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_OUTPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_OUTPUT structure


## -description


Contains the response to a <b>D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT</b> query.


## -struct-fields




### -field Output

A <a href="https://msdn.microsoft.com/D5650992-04D0-4DD2-A858-1E7FB979A9C2">D3D11_AUTHENTICATED_QUERY_OUTPUT</a> structure that contains a Message Authentication Code (MAC) and other data.


### -field DeviceHandle

A handle to the device.


### -field CryptoSessionHandle

A handle to the cryptographic session.


### -field OutputIDCount

The number of output IDs associated with the specified device and cryptographic session.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

