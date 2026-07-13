---
UID: NF:netfw.INetFwPolicy2.IsRuleGroupEnabled
title: INetFwPolicy2::IsRuleGroupEnabled (netfw.h)
description: Determines whether a specified group of firewall rules are enabled or disabled. (INetFwPolicy2.IsRuleGroupEnabled)
helpviewer_keywords: ["INetFwPolicy2 interface [ICS/ICF]","IsRuleGroupEnabled method","INetFwPolicy2.IsRuleGroupEnabled","INetFwPolicy2::IsRuleGroupEnabled","IsRuleGroupEnabled","IsRuleGroupEnabled method [ICS/ICF]","IsRuleGroupEnabled method [ICS/ICF]","INetFwPolicy2 interface","ics.inetfwpolicy2_isrulegroupenabled","netfw/INetFwPolicy2::IsRuleGroupEnabled"]
old-location: ics\inetfwpolicy2_isrulegroupenabled.htm
tech.root: ics
ms.assetid: b6f27763-6ceb-4bc3-be6f-f02908dc0387
ms.date: 12/05/2018
ms.keywords: INetFwPolicy2 interface [ICS/ICF],IsRuleGroupEnabled method, INetFwPolicy2.IsRuleGroupEnabled, INetFwPolicy2::IsRuleGroupEnabled, IsRuleGroupEnabled, IsRuleGroupEnabled method [ICS/ICF], IsRuleGroupEnabled method [ICS/ICF],INetFwPolicy2 interface, ics.inetfwpolicy2_isrulegroupenabled, netfw/INetFwPolicy2::IsRuleGroupEnabled
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
 - INetFwPolicy2::IsRuleGroupEnabled
 - netfw/INetFwPolicy2::IsRuleGroupEnabled
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
 - INetFwPolicy2.IsRuleGroupEnabled
---

# INetFwPolicy2::IsRuleGroupEnabled


## -description

The <b>IsRuleGroupEnabled</b> method determines whether a specified group of firewall rules are enabled or disabled.

## -parameters

### -param profileTypesBitmask [in]

A bitmask of profiles from <a href="/windows/win32/api/icftypes/ne-icftypes-net_fw_profile_type2">NET_FW_PROFILE_TYPE2</a>.

### -param group [in]

A string that was used to group rules together.  It can be the group name or an indirect string to the group name in the form of "@yourresourcedll.dll,-23255".  Rules belonging to this group would be queried.

### -param enabled [out]

Indicates whether the group of rules identified by the <i>group</i> parameter are enabled or disabled.  

If this value is set to true (<b>VARIANT_TRUE</b>), the group of rules is enabled; otherwise the group is disabled.

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
 This call  returns a boolean enable status which indicates whether the group of rules identified by the group parameter are enabled or disabled. If this value is set to true (VARIANT_TRUE), the group of rules is enabled; otherwise, the group is disabled.

## -remarks

When indirect strings in the form of "@yourresourcedll.dll,-23255" are passed as parameters to the Windows Firewall with Advanced Security APIs, they should either be placed under the System32 Windows directory or specified by a full path.  Further the file should have a secure access that permits the Local Service account read access to allow the Windows Firewall Service to read the strings.  To avoid non-privileged security principals from modifying the strings, the DLLs should only allow write access to the Administrator account.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2">INetFwPolicy2</a>
