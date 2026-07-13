---
UID: NF:wdspxe.PxeGetServerInfo
title: PxeGetServerInfo function (wdspxe.h)
description: Returns information about the PXE server. (PxeGetServerInfo)
helpviewer_keywords: ["PXE_GSI_TRACE_ENABLED","PxeGetServerInfo","PxeGetServerInfo function [Windows Deployment Services]","wds.pxegetserverinfo","wdspxe/PxeGetServerInfo"]
old-location: wds\pxegetserverinfo.htm
tech.root: wds
ms.assetid: 68fb12ff-c73c-4e36-8f62-de8a04a9afb0
ms.date: 12/05/2018
ms.keywords: PXE_GSI_TRACE_ENABLED, PxeGetServerInfo, PxeGetServerInfo function [Windows Deployment Services], wds.pxegetserverinfo, wdspxe/PxeGetServerInfo
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PxeGetServerInfo
 - wdspxe/PxeGetServerInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeGetServerInfo
---

# PxeGetServerInfo function


## -description

Returns information about the PXE server.

## -parameters

### -param uInfoType [in]

Selects the information that will be returned.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PXE_GSI_TRACE_ENABLED"></a><a id="pxe_gsi_trace_enabled"></a><dl>
<dt><b>PXE_GSI_TRACE_ENABLED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Returns a <b>BOOL</b> that indicates whether tracing is enabled for the 
        server. <b>TRUE</b> indicates that tracing is enabled.

</td>
</tr>
</table>

### -param pBuffer [out]

Address of a buffer that will receive the results of the query. The size and format of the results depends 
      on the value of the <i>uInfoType</i> parameter.

### -param uBufferLen [in]

Size of buffer pointed to by the <i>pBuffer</i> parameter.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>
