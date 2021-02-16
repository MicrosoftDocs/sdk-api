---
UID: NF:netcon.INetSharingManager.get_NetConnectionProps
title: INetSharingManager::get_NetConnectionProps (netcon.h)
description: The get_NetConnectionProps method retrieves a properties interface for the specified connection.
helpviewer_keywords: ["INetSharingManager interface [ICS/ICF]","get_NetConnectionProps method","INetSharingManager.get_NetConnectionProps","INetSharingManager::get_NetConnectionProps","_ics_inetsharingmanager_get_netconnectionprops","get_NetConnectionProps","get_NetConnectionProps method [ICS/ICF]","get_NetConnectionProps method [ICS/ICF]","INetSharingManager interface","ics.inetsharingmanager_get_netconnectionprops","netcon/INetSharingManager::get_NetConnectionProps"]
old-location: ics\inetsharingmanager_get_netconnectionprops.htm
tech.root: ics
ms.assetid: bf2db553-f324-4f23-b96e-f8ae703aa3ea
ms.date: 12/05/2018
ms.keywords: INetSharingManager interface [ICS/ICF],get_NetConnectionProps method, INetSharingManager.get_NetConnectionProps, INetSharingManager::get_NetConnectionProps, _ics_inetsharingmanager_get_netconnectionprops, get_NetConnectionProps, get_NetConnectionProps method [ICS/ICF], get_NetConnectionProps method [ICS/ICF],INetSharingManager interface, ics.inetsharingmanager_get_netconnectionprops, netcon/INetSharingManager::get_NetConnectionProps
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Hnetcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetSharingManager::get_NetConnectionProps
 - netcon/INetSharingManager::get_NetConnectionProps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetSharingManager.get_NetConnectionProps
---

# INetSharingManager::get_NetConnectionProps


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>get_NetConnectionProps</b> method retrieves a properties interface for the specified connection.

## -parameters

### -param pNetConnection [in]

Pointer to an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnection">INetConnection</a> interface for the connection for which to retrieve the properties interface.

### -param ppProps [out]

Pointer to an interface pointer that, on successful return, points to an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnectionprops">INetConnectionProps</a> interface for the connection.

## -returns

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
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A specified interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
A specified method is not implemented.

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
A pointer passed as a parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for unknown reasons.

</td>
</tr>
</table>

## -remarks

Not all connections can be configured for sharing. Retrieve the properties for the connection to verify that the connection can be shared before calling 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">INetSharingManager::get_INetSharingConfigurationForINetConnection</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager">INetSharingManager</a>



<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">INetSharingManager::get_INetSharingConfigurationForINetConnection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>