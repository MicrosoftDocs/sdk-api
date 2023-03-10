---
UID: NF:netfw.INetFwPolicy2.get_NotificationsDisabled
title: INetFwPolicy2::get_NotificationsDisabled (netfw.h)
description: Indicates whether interactive firewall notifications are disabled. (INetFwPolicy2.get_NotificationsDisabled)
helpviewer_keywords: ["INetFwPolicy2 interface [ICS/ICF]","NotificationsDisabled property","INetFwPolicy2.NotificationsDisabled","INetFwPolicy2.get_NotificationsDisabled","INetFwPolicy2::NotificationsDisabled","INetFwPolicy2::get_NotificationsDisabled","INetFwPolicy2::put_NotificationsDisabled","NotificationsDisabled property [ICS/ICF]","NotificationsDisabled property [ICS/ICF]","INetFwPolicy2 interface","get_NotificationsDisabled","ics.inetfwpolicy2_notificationsdisabled","netfw/INetFwPolicy2::NotificationsDisabled","netfw/INetFwPolicy2::get_NotificationsDisabled","netfw/INetFwPolicy2::put_NotificationsDisabled"]
old-location: ics\inetfwpolicy2_notificationsdisabled.htm
tech.root: ics
ms.assetid: 490442a4-3b60-4891-9d0e-71f8d2147999
ms.date: 12/05/2018
ms.keywords: INetFwPolicy2 interface [ICS/ICF],NotificationsDisabled property, INetFwPolicy2.NotificationsDisabled, INetFwPolicy2.get_NotificationsDisabled, INetFwPolicy2::NotificationsDisabled, INetFwPolicy2::get_NotificationsDisabled, INetFwPolicy2::put_NotificationsDisabled, NotificationsDisabled property [ICS/ICF], NotificationsDisabled property [ICS/ICF],INetFwPolicy2 interface, get_NotificationsDisabled, ics.inetfwpolicy2_notificationsdisabled, netfw/INetFwPolicy2::NotificationsDisabled, netfw/INetFwPolicy2::get_NotificationsDisabled, netfw/INetFwPolicy2::put_NotificationsDisabled
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
 - INetFwPolicy2::get_NotificationsDisabled
 - netfw/INetFwPolicy2::get_NotificationsDisabled
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
 - INetFwPolicy2.NotificationsDisabled
 - INetFwPolicy2.get_NotificationsDisabled
 - INetFwPolicy2.put_NotificationsDisabled
---

# INetFwPolicy2::get_NotificationsDisabled


## -description

Indicates whether interactive firewall notifications are disabled.

This property is read/write.

## -parameters

## -remarks

When you pass a profile type obtained from the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_currentprofiletypes">CurrentProfileTypes</a> property, make sure that you pass only one profile type to <b>get_NotificationsDisabled</b> and <b>put_NotificationsDisabled</b>. Note that <b>get_CurrentProfileTypes</b> can return multiple profiles.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2">INetFwPolicy2</a>
