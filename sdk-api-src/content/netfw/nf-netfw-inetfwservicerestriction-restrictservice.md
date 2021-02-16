---
UID: NF:netfw.INetFwServiceRestriction.RestrictService
title: INetFwServiceRestriction::RestrictService (netfw.h)
description: The RestrictService method turns service restriction on or off for a given service.
helpviewer_keywords: ["INetFwServiceRestriction interface [ICS/ICF]","RestrictService method","INetFwServiceRestriction.RestrictService","INetFwServiceRestriction::RestrictService","RestrictService","RestrictService method [ICS/ICF]","RestrictService method [ICS/ICF]","INetFwServiceRestriction interface","ics.inetfwservicerestriction_restrictservice","netfw/INetFwServiceRestriction::RestrictService"]
old-location: ics\inetfwservicerestriction_restrictservice.htm
tech.root: ics
ms.assetid: 5695bcb7-a83a-4581-8f46-00e85273b160
ms.date: 12/05/2018
ms.keywords: INetFwServiceRestriction interface [ICS/ICF],RestrictService method, INetFwServiceRestriction.RestrictService, INetFwServiceRestriction::RestrictService, RestrictService, RestrictService method [ICS/ICF], RestrictService method [ICS/ICF],INetFwServiceRestriction interface, ics.inetfwservicerestriction_restrictservice, netfw/INetFwServiceRestriction::RestrictService
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.dll: FirewallAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwServiceRestriction::RestrictService
 - netfw/INetFwServiceRestriction::RestrictService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwServiceRestriction.RestrictService
---

# INetFwServiceRestriction::RestrictService


## -description

The <b>RestrictService</b> method turns service restriction on or off for a given service.

## -parameters

### -param serviceName [in]

Name of the service for which service restriction is being turned on or off.

### -param appName [in]

Name of the application for which service restriction is being turned on or off.

### -param restrictService [in]

Indicates whether service restriction is being turned on or off.  If this value is true (<b>VARIANT_TRUE</b>), the service will be restricted when sending or receiving network traffic.  The Windows Service Hardening rules collection can contain rules which can allow this service specific inbound or outbound network access per specific requirements.  If false (<b>VARIANT_FALSE</b>), the service is not restricted by Windows Service Hardening.

### -param serviceSidRestricted [in]

Indicates the type of service SID for the specified service.  If this value is true (<b>VARIANT_TRUE</b>), the service SID will be restricted.  Otherwise, it will be unrestricted.

## -returns

<h3>C++</h3>
If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid parameter.

</td>
</tr>
</table>
 

<h3>VB</h3>
If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid parameter.

</td>
</tr>
</table>

## -remarks

When adding rules, note that there may be a small time lag before the newly-added rule is applied.

## -see-also

<a href="/windows/desktop/api/netfw/nn-netfw-inetfwservicerestriction">INetFwServiceRestriction</a>