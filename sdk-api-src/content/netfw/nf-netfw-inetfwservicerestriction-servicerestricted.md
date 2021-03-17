---
UID: NF:netfw.INetFwServiceRestriction.ServiceRestricted
title: INetFwServiceRestriction::ServiceRestricted (netfw.h)
description: The ServiceRestricted method indicates whether service restriction rules are enabled to limit traffic to the resources specified by the firewall rules.
helpviewer_keywords: ["INetFwServiceRestriction interface [ICS/ICF]","ServiceRestricted method","INetFwServiceRestriction.ServiceRestricted","INetFwServiceRestriction::ServiceRestricted","ServiceRestricted","ServiceRestricted method [ICS/ICF]","ServiceRestricted method [ICS/ICF]","INetFwServiceRestriction interface","ics.inetfwservicerestriction_servicerestricted","netfw/INetFwServiceRestriction::ServiceRestricted"]
old-location: ics\inetfwservicerestriction_servicerestricted.htm
tech.root: ics
ms.assetid: 38fe5a68-44ab-4bcb-8673-ebb1e87e446f
ms.date: 12/05/2018
ms.keywords: INetFwServiceRestriction interface [ICS/ICF],ServiceRestricted method, INetFwServiceRestriction.ServiceRestricted, INetFwServiceRestriction::ServiceRestricted, ServiceRestricted, ServiceRestricted method [ICS/ICF], ServiceRestricted method [ICS/ICF],INetFwServiceRestriction interface, ics.inetfwservicerestriction_servicerestricted, netfw/INetFwServiceRestriction::ServiceRestricted
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
 - INetFwServiceRestriction::ServiceRestricted
 - netfw/INetFwServiceRestriction::ServiceRestricted
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
 - INetFwServiceRestriction.ServiceRestricted
---

# INetFwServiceRestriction::ServiceRestricted


## -description

The <b>ServiceRestricted</b> method indicates whether service restriction rules are enabled to limit traffic to the resources specified by the firewall rules.

## -parameters

### -param serviceName [in]

Name of the service being queried concerning service restriction state.

### -param appName [in]

Name of the application being queried concerning service restriction state.

### -param serviceRestricted [out]

Indicates whether service restriction rules are in place to restrict the specified service.  If true (<b>VARIANT_TRUE</b>), service is restricted.  Otherwise, service is not restricted to the resources specified by firewall rules.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid pointer.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The method failed due to an invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/netfw/nn-netfw-inetfwservicerestriction">INetFwServiceRestriction</a>