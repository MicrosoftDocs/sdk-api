---
UID: NF:netfw.INetFwRule.get_Grouping
title: INetFwRule::get_Grouping (netfw.h)
description: Specifies the group to which an individual rule belongs. (Get)
helpviewer_keywords: ["Grouping property [ICS/ICF]","Grouping property [ICS/ICF]","INetFwRule interface","INetFwRule interface [ICS/ICF]","Grouping property","INetFwRule.Grouping","INetFwRule.get_Grouping","INetFwRule::Grouping","INetFwRule::get_Grouping","INetFwRule::put_Grouping","get_Grouping","ics.inetfwrule_grouping","netfw/INetFwRule::Grouping","netfw/INetFwRule::get_Grouping","netfw/INetFwRule::put_Grouping"]
old-location: ics\inetfwrule_grouping.htm
tech.root: ics
ms.assetid: 325b0c1d-3988-44ed-931c-6eed835f8c50
ms.date: 12/05/2018
ms.keywords: Grouping property [ICS/ICF], Grouping property [ICS/ICF],INetFwRule interface, INetFwRule interface [ICS/ICF],Grouping property, INetFwRule.Grouping, INetFwRule.get_Grouping, INetFwRule::Grouping, INetFwRule::get_Grouping, INetFwRule::put_Grouping, get_Grouping, ics.inetfwrule_grouping, netfw/INetFwRule::Grouping, netfw/INetFwRule::get_Grouping, netfw/INetFwRule::put_Grouping
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
 - INetFwRule::get_Grouping
 - netfw/INetFwRule::get_Grouping
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
 - INetFwRule.Grouping
 - INetFwRule.get_Grouping
 - INetFwRule.put_Grouping
---

# INetFwRule::get_Grouping


## -description

Specifies the group to which an individual rule belongs.

This property is read/write.

## -parameters

## -remarks

This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

Using the Grouping property is highly recommended, as it groups multiple rules into a single line in the Windows Firewall control panel. This allows the user to enable or disable multiple rules with a single click. The Grouping property can also be specified using indirect strings. In this case, a group description can also be specified that will appear in the rule group properties in the Windows Firewall control panel. For example, if the group string is specified by an indirect string at index 1005 ("@yourresources.dll,-1005"), the group description can be specified at a resource string higher by 10000 "@youresources.dll,-11005."

When indirect strings in the form of "h" are passed as parameters to the Windows Firewall with Advanced Security APIs, they should either be placed under the System32 Windows directory or specified by a full path.  Further, the file should have a secure access that permits the Local Service account read access to allow the Windows Firewall Service to read the strings.  To avoid non-privileged security principals from modifying the strings, the DLLs should only allow write access to the Administrator account.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>
