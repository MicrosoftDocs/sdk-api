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
 

 

