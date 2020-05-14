---
UID: NF:netcon.INetSharingManager.get_EnumPublicConnections
title: INetSharingManager::get_EnumPublicConnections (netcon.h)
description: The EnumPublicConnections method retrieves an enumeration interface for publicly-shared connections.helpviewer_keywords: ["INetSharingManager interface [ICS/ICF]","get_EnumPublicConnections method","INetSharingManager.get_EnumPublicConnections","INetSharingManager::get_EnumPublicConnections","_ics_inetsharingmanager_get_enumpublicconnections","get_EnumPublicConnections","get_EnumPublicConnections method [ICS/ICF]","get_EnumPublicConnections method [ICS/ICF]","INetSharingManager interface","ics.inetsharingmanager_get_enumpublicconnections","netcon/INetSharingManager::get_EnumPublicConnections"]
old-location: ics\inetsharingmanager_get_enumpublicconnections.htm
tech.root: ics
ms.assetid: 7db0eb73-8e0f-4267-9a88-20952f3721e2
ms.date: 12/05/2018
ms.keywords: INetSharingManager interface [ICS/ICF],get_EnumPublicConnections method, INetSharingManager.get_EnumPublicConnections, INetSharingManager::get_EnumPublicConnections, _ics_inetsharingmanager_get_enumpublicconnections, get_EnumPublicConnections, get_EnumPublicConnections method [ICS/ICF], get_EnumPublicConnections method [ICS/ICF],INetSharingManager interface, ics.inetsharingmanager_get_enumpublicconnections, netcon/INetSharingManager::get_EnumPublicConnections
f1_keywords:
- netcon/INetSharingManager.get_EnumPublicConnections
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Hnetcfg.dll
api_name:
- INetSharingManager.get_EnumPublicConnections
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetSharingManager::get_EnumPublicConnections


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The <b>EnumPublicConnections</b> method retrieves an enumeration interface for publicly-shared connections.


## -parameters




### -param Flags [in]

This parameter must be ICSSC_DEFAULT.


### -param ppColl [out]

Pointer to a pointer that, on successful return, points to an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingpublicconnectioncollection">INetSharingPublicConnectionCollection</a> interface.


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
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-ienumnetsharingpublicconnection">IEnumNetSharingPublicConnection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager">INetSharingManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingpublicconnectioncollection">INetSharingPublicConnectionCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

