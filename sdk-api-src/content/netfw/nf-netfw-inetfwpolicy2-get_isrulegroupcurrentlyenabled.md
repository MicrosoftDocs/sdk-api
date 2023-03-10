---
UID: NF:netfw.INetFwPolicy2.get_IsRuleGroupCurrentlyEnabled
title: INetFwPolicy2::get_IsRuleGroupCurrentlyEnabled (netfw.h)
description: Determines whether a specified group of firewall rules are enabled or disabled. (INetFwPolicy2.get_IsRuleGroupCurrentlyEnabled)
helpviewer_keywords: ["INetFwPolicy2 interface [ICS/ICF]","get_IsRuleGroupCurrentlyEnabled method","INetFwPolicy2.get_IsRuleGroupCurrentlyEnabled","INetFwPolicy2::get_IsRuleGroupCurrentlyEnabled","get_IsRuleGroupCurrentlyEnabled","get_IsRuleGroupCurrentlyEnabled method [ICS/ICF]","get_IsRuleGroupCurrentlyEnabled method [ICS/ICF]","INetFwPolicy2 interface","ics.inetfwpolicy2_isrulegroupcurrentlyenabled","netfw/INetFwPolicy2::get_IsRuleGroupCurrentlyEnabled"]
old-location: ics\inetfwpolicy2_isrulegroupcurrentlyenabled.htm
tech.root: ics
ms.assetid: 47a18291-398d-459f-b1e8-0bb7c8134e17
ms.date: 12/05/2018
ms.keywords: INetFwPolicy2 interface [ICS/ICF],get_IsRuleGroupCurrentlyEnabled method, INetFwPolicy2.get_IsRuleGroupCurrentlyEnabled, INetFwPolicy2::get_IsRuleGroupCurrentlyEnabled, get_IsRuleGroupCurrentlyEnabled, get_IsRuleGroupCurrentlyEnabled method [ICS/ICF], get_IsRuleGroupCurrentlyEnabled method [ICS/ICF],INetFwPolicy2 interface, ics.inetfwpolicy2_isrulegroupcurrentlyenabled, netfw/INetFwPolicy2::get_IsRuleGroupCurrentlyEnabled
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
 - INetFwPolicy2::get_IsRuleGroupCurrentlyEnabled
 - netfw/INetFwPolicy2::get_IsRuleGroupCurrentlyEnabled
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
 - INetFwPolicy2.get_IsRuleGroupCurrentlyEnabled
---

# INetFwPolicy2::get_IsRuleGroupCurrentlyEnabled


## -description

The <b>get_IsRuleGroupCurrentlyEnabled</b> method determines whether a specified group of firewall rules are enabled or disabled for the current profile.

## -parameters

### -param group [in]

A string that was used to group rules together.  It can be the group name or an indirect string to the group name in the form of "@C:\Program Files\Contoso Storefront\StorefrontRes.dll,-1234".  Rules belonging to this group would be queried.

### -param enabled [out]

Indicates whether the group of rules identified by the <i>group</i> parameter are enabled or disabled.  

If this value is set to true (<b>VARIANT_TRUE</b>), the group of rules is enabled; otherwise the group is disabled.

For Windows 7 and later, this value will be set to true (<b>VARIANT_TRUE</b>) if the rule group is enabled on at least one active profile.

## -returns

<h3>C++</h3>
 If the method succeeds, the  return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ACCESSDENIED</b></dt>
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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The method failed because a pointer was invalid.

</td>
</tr>
</table>
 

For Windows 7 and later, if multiple profiles are active and the profiles have different answers for <b>IsRuleGroupCurrentlyEnabled</b>, the return value is S_FALSE; if the profiles have the same answer for <b>IsRuleGroupCurrentlyEnabled</b>, the return value is S_TRUE. 

<h3>VB</h3>
 This call  returns a boolean enable status which indicates whether the group of rules identified by the group parameter are enabled or disabled. If this value is set to true (<b>VARIANT_TRUE</b>), the group of rules is enabled; otherwise, the group is disabled.

## -remarks

When indirect strings in the form of "@C:\Program Files\Contoso Storefront\StorefrontRes.dll,-1234" are passed as parameters to the Windows Firewall with Advanced Security APIs, they should be specified by a full path.  The file should have a secure access that permits the Local Service account read access to allow the Windows Firewall Service to read the strings.  To avoid non-privileged security principals from modifying the strings, the DLLs should only allow write access to the Administrator account.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2">INetFwPolicy2</a>



<a href="/previous-versions/windows/desktop/ics/rule-authoring">Rule Authoring</a>
