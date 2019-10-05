---
UID: NN:netfw.INetFwRule3
title: INetFwRule3 (netfw.h)
author: windows-sdk-content
description: Allows an application or service to access all the properties of INetFwRule2 and to provide access to the requirements of app containers.
old-location: ics\inetfwrule3.htm
tech.root: ics
ms.assetid: 72bf5ac3-7ee7-4837-96b2-815b499aac2f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetFwRule3, INetFwRule3 interface [ICS/ICF], INetFwRule3 interface [ICS/ICF],described, ics.inetfwrule3, netfw/INetFwRule3
ms.topic: interface
f1_keywords: 
 - "netfw/INetFwRule3"
dev_langs:
 - c++
req.header: netfw.h
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
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwRule3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwRule3 interface


## -description


The <b>INetFwRule3</b> interface allows an application or service to access all the properties of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule2">INetFwRule2</a> and to provide access to the requirements of app containers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwRule3</b> interface inherits from <b>INetFwRule2</b>. <b>INetFwRule3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwRule3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_localapppackageid">get_LocalAppPackageId</a>
</td>
<td align="left" width="63%">
Retrieves the LocalAppPackageId property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_localuserauthorizedlist">get_LocalUserAuthorizedList</a>
</td>
<td align="left" width="63%">
Retrieves the LocalUserAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_localuserowner">get_LocalUserOwner</a>
</td>
<td align="left" width="63%">
Retrieves the LocalUserOwner property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_remotemachineauthorizedlist">get_RemoteMachineAuthorizedList</a>
</td>
<td align="left" width="63%">
Retrieves the RemoteMachineAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_remoteuserauthorizedlist">get_RemoteUserAuthorizedList</a>
</td>
<td align="left" width="63%">
Retrieves the RemoteUserAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_secureflags">get_SecureFlags</a>
</td>
<td align="left" width="63%">
Retrieves the SecureFlags property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_localapppackageid">put_LocalAppPackageId</a>
</td>
<td align="left" width="63%">
Sets the LocalAppPackageId property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_localuserauthorizedlist">put_LocalUserAuthorizedList</a>
</td>
<td align="left" width="63%">
Sets the LocalUserAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_localuserowner">put_LocalUserOwner</a>
</td>
<td align="left" width="63%">
Sets the LocalUserOwner property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_remotemachineauthorizedlist">put_RemoteMachineAuthorizedList</a>
</td>
<td align="left" width="63%">
Sets the RemoteMachineAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_remoteuserauthorizedlist">put_RemoteUserAuthorizedList</a>
</td>
<td align="left" width="63%">
Sets the RemoteUserAuthorizedList property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_secureflags">put_SecureFlags</a>
</td>
<td align="left" width="63%">
Sets the SecureFlags property for this rule.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwRule3</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_localapppackageid">LocalAppPackageId</a>


</td>
<td align="left" width="63%">
Accesses the LocalAppPackageId property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_localuserauthorizedlist">LocalUserAuthorizedList</a>


</td>
<td align="left" width="63%">
Accesses the LocalUserAuthorizedList property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_localuserowner">LocalUserOwner</a>


</td>
<td align="left" width="63%">
Accesses the LocalUserOwner property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_remotemachineauthorizedlist">RemoteMachineAuthorizedList</a>


</td>
<td align="left" width="63%">
Accesses the RemoteMachineAuthorizedList property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_remoteuserauthorizedlist">RemoteUserAuthorizedList</a>


</td>
<td align="left" width="63%">
Accesses the RemoteUserAuthorizedList property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_secureflags">SecureFlags</a>


</td>
<td align="left" width="63%">
Accesses the SecureFlags property of this rule.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule2">INetFwRule2</a>
 

 

