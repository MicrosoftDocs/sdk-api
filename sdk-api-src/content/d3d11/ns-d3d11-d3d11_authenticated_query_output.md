---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_OUTPUT
title: D3D11_AUTHENTICATED_QUERY_OUTPUT
author: windows-sdk-content
description: Contains a response from the ID3D11VideoContext::QueryAuthenticatedChannel method.
old-location: mf\d3d11_authenticated_query_output.htm
tech.root: medfound
ms.assetid: D5650992-04D0-4DD2-A858-1E7FB979A9C2
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_OUTPUT, D3D11_AUTHENTICATED_QUERY_OUTPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_QUERY_OUTPUT, mf.d3d11_authenticated_query_output
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
 - D3D11_AUTHENTICATED_QUERY_OUTPUT
product: Windows
targetos: Windows
req.typenames: D3D11_AUTHENTICATED_QUERY_OUTPUT
req.redist: 
---

# D3D11_AUTHENTICATED_QUERY_OUTPUT structure


## -description


Contains a response from the <a href="https://msdn.microsoft.com/4E059358-E1FD-4EDB-B1D4-982802385232">ID3D11VideoContext::QueryAuthenticatedChannel</a> method.


## -struct-fields




### -field omac

A <a href="https://msdn.microsoft.com/68AEC018-1DFE-4811-A511-176E82C2E9E2">D3D11_OMAC</a> structure that contains a Message Authentication Code (MAC) of the data. The driver uses AESbased one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.


### -field QueryType

A GUID that specifies the query. For a list of possible values, see <a href="https://msdn.microsoft.com/D1FE4B31-A29D-4079-ABAE-8EB7DB0A0B42">D3D11_AUTHENTICATED_QUERY_INPUT</a>



### -field hChannel

A handle to the authenticated channel. To get the handle, call the <a href="https://msdn.microsoft.com/CA32D01B-B0B7-4F4F-8F48-747448DEC735">ID3D11AuthenticatedChannel::GetChannelHandle</a> method.


### -field SequenceNumber

The query sequence number.


### -field ReturnCode

The result code for the query.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

