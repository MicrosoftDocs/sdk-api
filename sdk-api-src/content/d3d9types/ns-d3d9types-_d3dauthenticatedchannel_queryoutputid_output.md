---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
title: "_D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT"
author: windows-driver-content
description: Contains the response to a D3DAUTHENTICATEDQUERY_OUTPUTID query.
old-location: mf\d3dauthenticatedchannel_queryoutputid_output.htm
old-project: medfound
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT, D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT structure [Media Foundation], D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT, D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT, d3d9types/D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT, mf.d3dauthenticatedchannel_queryoutputid_output
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT structure


## -description


Contains the response to a <a href="https://msdn.microsoft.com/7b56055a-fb36-4e54-9bee-ab9401b09267">D3DAUTHENTICATEDQUERY_OUTPUTID</a> query.

To send this query, call <a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a>.


## -struct-fields




### -field Output

 


### -field DeviceHandle

A handle to the device.


### -field CryptoSessionHandle

A handle to the cryptographic session.


### -field OutputIDIndex

The index of the output ID given in the <b>OutputID</b> member.


### -field OutputID

An output ID that is associated with the specified device and cryptographic session.


#### - D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT

A <a href="https://msdn.microsoft.com/b2783b8e-0436-419a-a93e-93dc1b87024d">D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT</a> structure that contains a Message Authentication Code (MAC) and other data.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a>
 

 

