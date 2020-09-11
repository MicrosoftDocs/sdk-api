---
UID: NF:ndfapi.NdfCreatePnrpIncident
title: NdfCreatePnrpIncident function (ndfapi.h)
description: Creates a session to diagnose issues with the Peer Name Resolution Protocol (PNRP) service.
helpviewer_keywords: ["NdfCreatePnrpIncident","NdfCreatePnrpIncident function [NDF]","ndf.ndfcreatepnrpincident","ndfapi/NdfCreatePnrpIncident"]
old-location: ndf\ndfcreatepnrpincident.htm
tech.root: NDF
ms.assetid: e9ee6433-89b9-4b95-b02c-2778e009220c
ms.date: 12/05/2018
ms.keywords: NdfCreatePnrpIncident, NdfCreatePnrpIncident function [NDF], ndf.ndfcreatepnrpincident, ndfapi/NdfCreatePnrpIncident
req.header: ndfapi.h
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
req.lib: Ndfapi.lib
req.dll: Ndfapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NdfCreatePnrpIncident
 - ndfapi/NdfCreatePnrpIncident
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ndfapi.dll
api_name:
 - NdfCreatePnrpIncident
---

# NdfCreatePnrpIncident function


## -description

The <b>NdfCreatePnrpIncident</b> function creates  a session to diagnose issues with the Peer Name Resolution Protocol (PNRP) service.

## -parameters

### -param cloudname [in]

Type: <b>LPCWSTR</b>

The name of the cloud to be diagnosed.

### -param peername [in, optional]

Type: <b>LPCWSTR</b>

Optional name of a peer node which PNRP can attempt to resolve. The results will be used to help diagnose any problems.

### -param diagnosePublish [in]

Type: <b>BOOL</b>

Specifies whether the helper class should verify that the node can publish IDs. If <b>FALSE</b>, this diagnostic step will be skipped.

### -param appId [in, optional]

Type: <b>LPCWSTR</b>

Application ID for the calling application.

### -param handle [out]

Type: <b>NDFHANDLE*</b>

Handle to the Network Diagnostics Framework incident.

## -returns

Type: <b>HRESULT</b>

Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDF_E_BAD_PARAM</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters has not been provided correctly.


</td>
</tr>
</table>

## -remarks

The level of diagnosis performed depends on the parameters supplied. The availability of the PNRP service and the availability of the IPv6 networking class will be diagnosed, and additional diagnosis will be performed if certain parameters are supplied.<ul>
<li>If <i>peername</i> is specified, NDF will validate the availability of that peer in the PNRP network.</li>
<li>If <i>diagnosePublish</i> is specified, NDF will validate the ability to publish a name in PNRP.</li>
</ul>

