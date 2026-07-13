---
UID: NF:netfw.INetFwOpenPort.get_Enabled
title: INetFwOpenPort::get_Enabled (netfw.h)
description: Indicates whether the settings for this port are currently enabled. (Get)
helpviewer_keywords: ["Enabled property [ICS/ICF]","Enabled property [ICS/ICF]","INetFwOpenPort interface","INetFwOpenPort interface [ICS/ICF]","Enabled property","INetFwOpenPort.Enabled","INetFwOpenPort.get_Enabled","INetFwOpenPort::Enabled","INetFwOpenPort::get_Enabled","INetFwOpenPort::put_Enabled","get_Enabled","ics.inetfwopenport_enabled","netfw/INetFwOpenPort::Enabled","netfw/INetFwOpenPort::get_Enabled","netfw/INetFwOpenPort::put_Enabled"]
old-location: ics\inetfwopenport_enabled.htm
tech.root: ics
ms.assetid: f4fc7a4f-abc5-486a-89c8-dfea17770f3c
ms.date: 12/05/2018
ms.keywords: Enabled property [ICS/ICF], Enabled property [ICS/ICF],INetFwOpenPort interface, INetFwOpenPort interface [ICS/ICF],Enabled property, INetFwOpenPort.Enabled, INetFwOpenPort.get_Enabled, INetFwOpenPort::Enabled, INetFwOpenPort::get_Enabled, INetFwOpenPort::put_Enabled, get_Enabled, ics.inetfwopenport_enabled, netfw/INetFwOpenPort::Enabled, netfw/INetFwOpenPort::get_Enabled, netfw/INetFwOpenPort::put_Enabled
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
 - INetFwOpenPort::get_Enabled
 - netfw/INetFwOpenPort::get_Enabled
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
 - INetFwOpenPort.Enabled
 - INetFwOpenPort.get_Enabled
 - INetFwOpenPort.put_Enabled
---

# INetFwOpenPort::get_Enabled


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether the settings for this port are currently enabled.

This property is read/write.

## -parameters

## -remarks

This property can be set to false (<b>VARIANT_FALSE</b>) to allow port settings to be stored in the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenports">INetFWOpenPorts</a> collection without actually opening the port. 

The default value is true (<b>VARIANT_TRUE</b>) for new ports.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenports">INetFWOpenPorts</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenport">INetFwOpenPort</a>
