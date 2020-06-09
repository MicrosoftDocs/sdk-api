---
UID: NF:netfw.INetFwPolicy2.get_DefaultInboundAction
title: INetFwPolicy2::get_DefaultInboundAction (netfw.h)
description: Specifies the default action for inbound traffic. These settings are Block by default.
helpviewer_keywords: ["DefaultInboundAction property [ICS/ICF]","DefaultInboundAction property [ICS/ICF]","INetFwPolicy2 interface","INetFwPolicy2 interface [ICS/ICF]","DefaultInboundAction property","INetFwPolicy2.DefaultInboundAction","INetFwPolicy2.get_DefaultInboundAction","INetFwPolicy2::DefaultInboundAction","INetFwPolicy2::get_DefaultInboundAction","INetFwPolicy2::put_DefaultInboundAction","get_DefaultInboundAction","ics.inetfwpolicy2_defaultinboundaction","netfw/INetFwPolicy2::DefaultInboundAction","netfw/INetFwPolicy2::get_DefaultInboundAction","netfw/INetFwPolicy2::put_DefaultInboundAction"]
old-location: ics\inetfwpolicy2_defaultinboundaction.htm
tech.root: ics
ms.assetid: d9251979-0479-4245-8a29-a161acbf591f
ms.date: 12/05/2018
ms.keywords: DefaultInboundAction property [ICS/ICF], DefaultInboundAction property [ICS/ICF],INetFwPolicy2 interface, INetFwPolicy2 interface [ICS/ICF],DefaultInboundAction property, INetFwPolicy2.DefaultInboundAction, INetFwPolicy2.get_DefaultInboundAction, INetFwPolicy2::DefaultInboundAction, INetFwPolicy2::get_DefaultInboundAction, INetFwPolicy2::put_DefaultInboundAction, get_DefaultInboundAction, ics.inetfwpolicy2_defaultinboundaction, netfw/INetFwPolicy2::DefaultInboundAction, netfw/INetFwPolicy2::get_DefaultInboundAction, netfw/INetFwPolicy2::put_DefaultInboundAction
f1_keywords:
- netfw/INetFwPolicy2.DefaultInboundAction
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FirewallAPI.dll
api_name:
- INetFwPolicy2.DefaultInboundAction
- INetFwPolicy2.get_DefaultInboundAction
- INetFwPolicy2.put_DefaultInboundAction
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwPolicy2::get_DefaultInboundAction


## -description


Specifies the default action for inbound traffic. These settings are Block by default.

This property is read/write.


## -parameters


## -remarks



All interfaces are firewall-enabled. This means that all the exceptions (such as GloballyOpenPorts, Applications, or Services) which are  specified in the profile, are ignored
   and only locally-initiated traffic is allowed.

When you pass a profile type obtained from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_currentprofiletypes">CurrentProfileTypes</a> property, make sure that you pass only one profile type to <b>get_DefaultInboundAction</b> and <b>put_DefaultInboundAction</b>. Note that <b>get_CurrentProfileTypes</b> can return multiple profiles.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2">INetFwPolicy2</a>



<a href="https://docs.microsoft.com/en-us/windows/win32/api/icftypes/ne-icftypes-net_fw_action">NET_FW_ACTION</a>



<a href="https://docs.microsoft.com/en-us/windows/win32/api/icftypes/ne-icftypes-net_fw_profile_type2">NET_FW_PROFILE_TYPE2</a>
 

 

