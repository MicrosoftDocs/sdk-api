---
UID: NF:mprapi.MprConfigBufferFree
title: MprConfigBufferFree function (mprapi.h)
description: The MprConfigBufferFree function frees buffers. MprConfigXEnum, MprConfigXGetInfo
helpviewer_keywords: ["MprConfigBufferFree","MprConfigBufferFree function [RAS]","_mpr_mprconfigbufferfree","mprapi/MprConfigBufferFree","rras.mprconfigbufferfree"]
old-location: rras\mprconfigbufferfree.htm
tech.root: RRAS
ms.assetid: d7df56ee-72e4-4b0c-87a3-a1f66d791b62
ms.date: 12/05/2018
ms.keywords: MprConfigBufferFree, MprConfigBufferFree function [RAS], _mpr_mprconfigbufferfree, mprapi/MprConfigBufferFree, rras.mprconfigbufferfree
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprConfigBufferFree
 - mprapi/MprConfigBufferFree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprConfigBufferFree
---

# MprConfigBufferFree function


## -description

The 
<b>MprConfigBufferFree</b> function frees buffers allocated by calls to the following functions:

MprConfigXEnum
			

MprConfigXGetInfo
			

where X stands for Server, 
<a href="/windows/desktop/RRAS/interface">Interface</a>, Transport, or InterfaceTransport.

## -parameters

### -param pBuffer [in]

Pointer to a memory buffer allocated by a previous call to: 




MprConfigXEnum
						

MprConfigXGetInfo
						

where X stands for Server, 
<a href="/windows/desktop/RRAS/interface">Interface</a>, Transport, or InterfaceTransport.

## -returns

If the function succeeds, the return value is NO_ERROR.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfaceenum">MprConfigInterfaceEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegetinfo">MprConfigInterfaceGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportenum">MprConfigInterfaceTransportEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo">MprConfigInterfaceTransportGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigservergetinfo">MprConfigServerGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportenum">MprConfigTransportEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportgetinfo">MprConfigTransportGetInfo</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>