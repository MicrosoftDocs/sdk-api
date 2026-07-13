---
UID: NN:netfw.INetFwRemoteAdminSettings
title: INetFwRemoteAdminSettings (netfw.h)
description: The INetFwRemoteAdminSettings interface provides access to the settings that control remote administration.
helpviewer_keywords: ["INetFwRemoteAdminSettings","INetFwRemoteAdminSettings interface [ICS/ICF]","INetFwRemoteAdminSettings interface [ICS/ICF]","described","ics.inetfwremoteadminsettings","netfw/INetFwRemoteAdminSettings"]
old-location: ics\inetfwremoteadminsettings.htm
tech.root: ics
ms.assetid: 35f34a53-e73b-48be-ac79-9b7ab825c6ad
ms.date: 12/05/2018
ms.keywords: INetFwRemoteAdminSettings, INetFwRemoteAdminSettings interface [ICS/ICF], INetFwRemoteAdminSettings interface [ICS/ICF],described, ics.inetfwremoteadminsettings, netfw/INetFwRemoteAdminSettings
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
 - INetFwRemoteAdminSettings
 - netfw/INetFwRemoteAdminSettings
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
 - INetFwRemoteAdminSettings
---

# INetFwRemoteAdminSettings interface


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwRemoteAdminSettings</b> interface provides access to the settings that control remote administration.

## -inheritance

The <b>INetFwRemoteAdminSettings</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwRemoteAdminSettings</b> also has these types of members:

## -remarks

An
instance of this interface is retrieved through the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_remoteadminsettings">RemoteAdminSettings</a> property of the INetFwProfile interface. 

All configuration changes take
 effect immediately.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwprofile">INetFwProfile</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
