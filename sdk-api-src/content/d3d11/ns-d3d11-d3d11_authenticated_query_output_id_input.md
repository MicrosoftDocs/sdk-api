---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT
title: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT
author: windows-sdk-content
description: Contains input data for a D3D11_AUTHENTICATED_QUERY_OUTPUT_ID query.
old-location: mf\d3d11_authenticated_query_output_id_input.htm
tech.root: medfound
ms.assetid: 2F4A6248-77DB-479B-B16C-81C3EE22937A
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT, D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT, mf.d3d11_authenticated_query_output_id_input
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT
product: Windows
targetos: Windows
req.typenames: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT
req.redist: 
---

# D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT structure


## -description


Contains input data for a <b>D3D11_AUTHENTICATED_QUERY_OUTPUT_ID</b> query.


## -struct-fields




### -field Input

A <a href="https://msdn.microsoft.com/D1FE4B31-A29D-4079-ABAE-8EB7DB0A0B42">D3D11_AUTHENTICATED_QUERY_INPUT</a> structure that contains the GUID for the query and other data.


### -field DeviceHandle

A handle to the device.


### -field CryptoSessionHandle

A handle to the cryptographic session.


### -field OutputIDIndex

The index of the output ID.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

