---
UID: NF:netfw.INetFwPolicy2.EnableRuleGroup
title: INetFwPolicy2::EnableRuleGroup (netfw.h)
description: Enables or disables a specified group of firewall rules.
helpviewer_keywords: ["EnableRuleGroup","EnableRuleGroup method [ICS/ICF]","EnableRuleGroup method [ICS/ICF]","INetFwPolicy2 interface","INetFwPolicy2 interface [ICS/ICF]","EnableRuleGroup method","INetFwPolicy2.EnableRuleGroup","INetFwPolicy2::EnableRuleGroup","ics.inetfwpolicy2_enablerulegroup","netfw/INetFwPolicy2::EnableRuleGroup"]
old-location: ics\inetfwpolicy2_enablerulegroup.htm
tech.root: ics
ms.assetid: fceb9562-b8de-4ccd-9d3e-4a4a4784a35f
ms.date: 12/05/2018
ms.keywords: EnableRuleGroup, EnableRuleGroup method [ICS/ICF], EnableRuleGroup method [ICS/ICF],INetFwPolicy2 interface, INetFwPolicy2 interface [ICS/ICF],EnableRuleGroup method, INetFwPolicy2.EnableRuleGroup, INetFwPolicy2::EnableRuleGroup, ics.inetfwpolicy2_enablerulegroup, netfw/INetFwPolicy2::EnableRuleGroup
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
 - INetFwPolicy2::EnableRuleGroup
 - netfw/INetFwPolicy2::EnableRuleGroup
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
 - INetFwPolicy2.EnableRuleGroup
---

# INetFwPolicy2::EnableRuleGroup


## -description

The <b>EnableRuleGroup</b> method enables or disables a specified group of firewall rules.

## -parameters

### -param profileTypesBitmask [in]

A bitmask of profiles from <a href="/windows/win32/api/icftypes/ne-icftypes-net_fw_profile_type2">NET_FW_PROFILE_TYPE2</a>.

### -param group [in]

A string that was used to group rules together.  It can be the group name or an indirect string to the group name in the form of "@C:\Program Files\Contoso Storefront\StorefrontRes.dll,-1234".  Rules belonging to this group would be enabled or disabled.

### -param enable [in]

Indicates whether the group of rules identified by the <i>group</i> parameter are to be enabled or disabled.

If this value is set to true (<b>VARIANT_TRUE</b>), the group of rules will be enabled; otherwise the group is disabled.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The requested group does not exist.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The requested group does not exist.

</td>
</tr>
</table>

## -remarks

When indirect strings in the form of "@C:\Program Files\Contoso Storefront\StorefrontRes.dll,-1234" are passed as parameters to the Windows Firewall with Advanced Security APIs, they should be specified by a full path.  The file should have a secure access that permits the Local Service account read access to allow the Windows Firewall Service to read the strings.  To avoid non-privileged security principals from modifying the strings, the DLLs should only allow write access to the Administrator account.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2">INetFwPolicy2</a>



<a href="/previous-versions/windows/desktop/ics/rule-authoring">Rule Authoring</a>