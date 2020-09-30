---
UID: NS:naptypes.tagNetworkSoH
title: NetworkSoH (naptypes.h)
description: Defines the wire SoH protocol.
helpviewer_keywords: ["NetworkSoH","NetworkSoH structure [NAP]","NetworkSoHRequest","NetworkSoHRequest structure [NAP]","NetworkSoHResponse","NetworkSoHResponse structure [NAP]","nap.networksoh_struct","naptypes/NetworkSoH","naptypes/NetworkSoHRequest","naptypes/NetworkSoHResponse"]
old-location: nap\networksoh_struct.htm
tech.root: NAP
ms.assetid: 7b1d4563-4758-40d8-be6c-51533bbcb09e
ms.date: 12/05/2018
ms.keywords: NetworkSoH, NetworkSoH structure [NAP], NetworkSoHRequest, NetworkSoHRequest structure [NAP], NetworkSoHResponse, NetworkSoHResponse structure [NAP], nap.networksoh_struct, naptypes/NetworkSoH, naptypes/NetworkSoHRequest, naptypes/NetworkSoHResponse
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
targetos: Windows
req.typenames: NetworkSoH, NetworkSoHRequest, NetworkSoHResponse
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNetworkSoH
 - naptypes/tagNetworkSoH
 - NetworkSoH
 - naptypes/NetworkSoH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - NetworkSoH
---

# NetworkSoH structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>NetworkSoH</b> structure defines the wire SoH protocol.

## -struct-fields

### -field size

The size, in bytes, of the data blob in the range <a href="/windows/desktop/NAP/nap-type-constants">minNetworkSoHSize</a> to <b>maxNetworkSoHSize</b>.

### -field data

A pointer to a data blob that contains the <a href="/windows/desktop/api/naptypes/ns-naptypes-soh">SoH</a> structure in network byte order.

## -see-also

<a href="/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="/windows/desktop/NAP/nap-structures">NAP Structures</a>