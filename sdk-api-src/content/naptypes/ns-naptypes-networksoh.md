---
UID: NS:naptypes.tagNetworkSoH
title: NetworkSoH (naptypes.h)
author: windows-sdk-content
description: Defines the wire SoH protocol.
old-location: nap\networksoh_struct.htm
tech.root: NAP
ms.assetid: 7b1d4563-4758-40d8-be6c-51533bbcb09e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NetworkSoH, NetworkSoH structure [NAP], NetworkSoHRequest, NetworkSoHRequest structure [NAP], NetworkSoHResponse, NetworkSoHResponse structure [NAP], nap.networksoh_struct, naptypes/NetworkSoH, naptypes/NetworkSoHRequest, naptypes/NetworkSoHResponse
ms.topic: struct
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
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
 - NapTypes.h
api_name:
 - NetworkSoH
product: Windows
targetos: Windows
req.typenames: NetworkSoH, NetworkSoHRequest, NetworkSoHResponse
req.redist: 
ms.custom: 19H1
---

# NetworkSoH structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>NetworkSoH</b> structure defines the wire SoH protocol.


## -struct-fields




### -field size

The size, in bytes, of the data blob in the range <a href="https://msdn.microsoft.com/2727487c-8c6a-4cd9-b6d8-253191a7d7f6">minNetworkSoHSize</a> to <b>maxNetworkSoHSize</b>. 


### -field data

A pointer to a data blob that contains the <a href="https://msdn.microsoft.com/6db0303d-ab33-4fb9-90a2-b909b2781ba5">SoH</a> structure in network byte order.


## -see-also




<a href="https://msdn.microsoft.com/e391be3c-95ab-4c80-a5d8-8a8fef28e56b">NAP Reference</a>



<a href="https://msdn.microsoft.com/68048587-0f7e-48d4-9326-768a977ea3ee">NAP Structures</a>
 

 

