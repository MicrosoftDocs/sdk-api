---
UID: NS:d3d9types._D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
title: "_D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE"
author: windows-driver-content
description: Contains input data for a D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE command.
old-location: mf\d3dauthenticatedchannel_configuresharedresource.htm
old-project: medfound
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE, D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE structure [Media Foundation], _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE, d3d9types/D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE, mf.d3dauthenticatedchannel_configuresharedresource
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
req.typenames: D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE structure


## -description


Contains input data for a <a href="https://msdn.microsoft.com/5fa2b88f-e946-436c-953e-04e0e338146c">D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE</a> command.

To send this query, call <a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>.


## -struct-fields




### -field Parameters

A <a href="https://msdn.microsoft.com/7646100e-f768-4935-9e71-1d9db0d69c52">D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT</a> structure that contains the command GUID and other data.


### -field ProcessIdentiferType

A <a href="https://msdn.microsoft.com/8878905e-f55b-4dbc-9608-da0082daf673">D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE</a> value that specifies the type of process.

To specify the Desktop Window Manager (DWM) process, set this member to <b>PROCESSIDTYPE_DWM</b>. Otherwise, set this member to <b>PROCESSIDTYPE_HANDLE</b> and set the <b>ProcessHandle</b> member to a valid handle.


### -field ProcessHandle

A process handle. If the <b>ProcessIdentifier</b> member equals <b>PROCESSTIDTYPE_HANDLE</b>, the <b>ProcessHandle</b> member specifies a handle to a process. Otherwise, the value is ignored.


### -field AllowAccess

If <b>TRUE</b>, the specified process has access to restricted shared resources.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">IDirect3DAuthenticatedChannel9::Configure</a>
 

 

