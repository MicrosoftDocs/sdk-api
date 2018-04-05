---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
title: "_D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT"
author: windows-driver-content
description: Contains the response to a D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS query.
old-location: mf\d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output.htm
old-project: medfound
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT, D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT, d3d9types/D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT, mf.d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output
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
req.typenames: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT structure


## -description


Contains the response to a <a href="https://msdn.microsoft.com/669d9623-3a96-4661-9dae-3f283a990fe8">D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS</a> query.

To send this query, call <a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a>.


## -struct-fields




### -field Output

A <a href="https://msdn.microsoft.com/b2783b8e-0436-419a-a93e-93dc1b87024d">D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT</a> structure that contains a Message Authentication Code (MAC) and other data.


### -field ProcessIndex

The index of the process in the list of processes.


### -field ProcessIdentifer

A <a href="https://msdn.microsoft.com/8878905e-f55b-4dbc-9608-da0082daf673">D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE</a> value that specifies the type of process.


### -field ProcessHandle

A process handle. If the <b>ProcessIdentifier</b> member equals <b>PROCESSIDTYPE_HANDLE</b>, the <b>ProcessHandle</b> member contains a valid handle to a process. Otherwise, this member is ignored.


## -remarks



The Desktop Window Manager (DWM) process is identified by setting <b>ProcessIdentifier</b> equal to <b>PROCESSIDTYPE_DWM</b>. Other processes are identified by setting the process handle in <b>ProcessHandle</b> and setting <b>ProcessIdentifier</b> equal to <b>PROCESSIDTYPE_HANDLE</b>.




## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">IDirect3DAuthenticatedChannel9::Query</a>
 

 

