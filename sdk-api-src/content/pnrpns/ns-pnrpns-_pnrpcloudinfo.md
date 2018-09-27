---
UID: NS:pnrpns._PNRPCLOUDINFO
title: "_PNRPCLOUDINFO"
author: windows-sdk-content
description: The PNRPCLOUDINFO structure is pointed to by the lpBlob member of the WSAQUERYSET structure.
old-location: p2p\pnrpcloudinfo.htm
tech.root: p2psdk
ms.assetid: 82af5a4f-1b29-405a-a200-1d723ea7693b
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PPNRPCLOUDINFO, PNRPCLOUDINFO, PNRPCLOUDINFO structure [Peer Networking], PPNRPCLOUDINFO, PPNRPCLOUDINFO structure pointer [Peer Networking], _PNRPCLOUDINFO, p2p.pnrpcloudinfo, pnrpns/PNRPCLOUDINFO, pnrpns/PPNRPCLOUDINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: pnrpns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Pnrpns.h
api_name:
 - PNRPCLOUDINFO
product: Windows
targetos: Windows
req.typenames: PNRPCLOUDINFO, *PPNRPCLOUDINFO
req.redist: 
---

# _PNRPCLOUDINFO structure


## -description


The <b>PNRPCLOUDINFO</b> structure is pointed to by the <b>lpBlob</b> member of the <a href="https://msdn.microsoft.com/e0af2cd9-9cbf-44a1-aa4d-4df211b04782">WSAQUERYSET</a> structure.


## -struct-fields




### -field dwSize

Specifies the size of this structure.


### -field Cloud

Specifies the network cloud information stored in a <a href="https://msdn.microsoft.com/8187ce9e-e1a9-4dce-902e-8a1c43b4b047">PNRP_CLOUD_ID</a> structure.


### -field enCloudState

Specifies the state of the network cloud. Valid values are specified by <a href="https://msdn.microsoft.com/0263d742-f82b-4158-9343-86a8abf4cde1">PNRP_CLOUD_STATE</a>.


### -field enCloudFlags

Indicates if the cloud name is valid on the network or only valid on the current computer. Valid values are specified by <a href="https://msdn.microsoft.com/7c3750a0-95aa-460b-bdf3-6796751d7c9b">PNRP_CLOUD_FLAGS</a>.


## -see-also




<a href="https://msdn.microsoft.com/e92ecb14-3f3a-48bb-963b-0c6e58c54089">PNRP and BLOB</a>



<a href="https://msdn.microsoft.com/71cca892-89e7-44d1-920d-987587eeed50">PNRP and WSALookupServiceBegin</a>



<a href="https://msdn.microsoft.com/b3e1abf4-ff59-481d-b96e-f8916a47cd52">PNRP and WSALookupServiceNext</a>



<a href="https://msdn.microsoft.com/0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b">PNRP and WSAQUERYSET</a>



<a href="https://msdn.microsoft.com/7c3750a0-95aa-460b-bdf3-6796751d7c9b">PNRP_CLOUD_FLAGS</a>



<a href="https://msdn.microsoft.com/8187ce9e-e1a9-4dce-902e-8a1c43b4b047">PNRP_CLOUD_ID</a>



<a href="https://msdn.microsoft.com/0263d742-f82b-4158-9343-86a8abf4cde1">PNRP_CLOUD_STATE</a>



<a href="https://msdn.microsoft.com/e0af2cd9-9cbf-44a1-aa4d-4df211b04782">WSAQUERYSET</a>
 

 

