---
UID: NF:netfw.INetFwServices.Item
title: INetFwServices::Item (netfw.h)
description: Returns the specified service if it is in the collection.
helpviewer_keywords: ["INetFwServices interface [ICS/ICF]","Item method","INetFwServices.Item","INetFwServices::Item","Item","Item method [ICS/ICF]","Item method [ICS/ICF]","INetFwServices interface","ics.inetfwservices_item","netfw/INetFwServices::Item"]
old-location: ics\inetfwservices_item.htm
tech.root: ics
ms.assetid: a13740cc-7d9a-4c1f-ae18-a31ca4d39b54
ms.date: 12/05/2018
ms.keywords: INetFwServices interface [ICS/ICF],Item method, INetFwServices.Item, INetFwServices::Item, Item, Item method [ICS/ICF], Item method [ICS/ICF],INetFwServices interface, ics.inetfwservices_item, netfw/INetFwServices::Item
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwServices::Item
 - netfw/INetFwServices::Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwServices.Item
---

# INetFwServices::Item


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Returns the specified service if it is in the collection.

## -parameters

### -param svcType [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
Type of  service to fetch.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
Type of  service to fetch. See <a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_service_type">NET_FW_SERVICE_TYPE</a>


</td>
</tr>
</table>

### -param service [out]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
Reference to the returned <b>INetFwService</b> object.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
Reference to the returned <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwservice">INetFwService</a> object.

</td>
</tr>
</table>

## -returns

<h3>C++</h3>
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
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The method failed because the requested item does not exist.

</td>
</tr>
</table>
 

<h3>VB</h3>
If the method succeeds, the return value is S_OK.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The method failed because the requested item does not exist.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwservice">INetFwService</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwservices">INetFwServices</a>



<a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_service_type">NET_FW_SERVICE_TYPE</a>