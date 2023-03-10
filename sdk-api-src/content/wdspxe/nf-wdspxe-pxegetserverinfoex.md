---
UID: NF:wdspxe.PxeGetServerInfoEx
title: PxeGetServerInfoEx function (wdspxe.h)
description: Returns information about the PXE server. (PxeGetServerInfoEx)
helpviewer_keywords: ["PXE_GSI_SERVER_DUID","PXE_GSI_TRACE_ENABLED","PxeGetServerInfoEx","PxeGetServerInfoEx function [Windows Deployment Services]","wds.pxegetserverinfoex","wdspxe/PxeGetServerInfoEx"]
old-location: wds\pxegetserverinfoex.htm
tech.root: wds
ms.assetid: E0AD1507-3018-42B5-B4DD-E19CC49FD25F
ms.date: 12/05/2018
ms.keywords: PXE_GSI_SERVER_DUID, PXE_GSI_TRACE_ENABLED, PxeGetServerInfoEx, PxeGetServerInfoEx function [Windows Deployment Services], wds.pxegetserverinfoex, wdspxe/PxeGetServerInfoEx
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - PxeGetServerInfoEx
 - wdspxe/PxeGetServerInfoEx
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
 - PxeGetServerInfoEx
---

# PxeGetServerInfoEx function


## -description

Returns information about the PXE server.

For more information about the OPTION_SERVERID option, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="https://www.ietf.org/rfc/rfc3315.txt">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).

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
<tr>
<td width="40%"><a id="PXE_GSI_SERVER_DUID"></a><a id="pxe_gsi_server_duid"></a><dl>
<dt><b>PXE_GSI_SERVER_DUID</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
 Returns a byte array that corresponds to the DHCPv6 DUID that is sent to DHCPv6 PXE clients in response packets in the OPTION_SERVERID option.  <b>PXE_GSI_SERVER_DUID</b> cannot be used with <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxegetserverinfo">PxeGetServerInfo</a>.

</td>
</tr>
</table>

### -param pBuffer [out]

Address of a buffer that will receive the results of the query. The size and format of the results depends 
      on the value of the <i>uInfoType</i> parameter.

### -param uBufferLen [in]

Size of buffer pointed to by the <i>pBuffer</i> parameter.

### -param puBufferUsed [out]

Size of buffer pointed to by the <i>pBuffer</i> parameter.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>
