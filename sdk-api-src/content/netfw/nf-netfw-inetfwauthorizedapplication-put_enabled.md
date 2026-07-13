---
UID: NF:netfw.INetFwAuthorizedApplication.put_Enabled
title: INetFwAuthorizedApplication::put_Enabled (netfw.h)
description: Indicates whether the settings for this application are currently enabled. (Put)
helpviewer_keywords: ["Enabled property [ICS/ICF]","Enabled property [ICS/ICF]","INetFwAuthorizedApplication interface","INetFwAuthorizedApplication interface [ICS/ICF]","Enabled property","INetFwAuthorizedApplication.Enabled","INetFwAuthorizedApplication.put_Enabled","INetFwAuthorizedApplication::Enabled","INetFwAuthorizedApplication::get_Enabled","INetFwAuthorizedApplication::put_Enabled","ics.inetfwauthorizedapplication_enabled","netfw/INetFwAuthorizedApplication::Enabled","netfw/INetFwAuthorizedApplication::get_Enabled","netfw/INetFwAuthorizedApplication::put_Enabled","put_Enabled"]
old-location: ics\inetfwauthorizedapplication_enabled.htm
tech.root: ics
ms.assetid: 03a1503e-aee5-484f-8a4c-a7e10dffe401
ms.date: 12/05/2018
ms.keywords: Enabled property [ICS/ICF], Enabled property [ICS/ICF],INetFwAuthorizedApplication interface, INetFwAuthorizedApplication interface [ICS/ICF],Enabled property, INetFwAuthorizedApplication.Enabled, INetFwAuthorizedApplication.put_Enabled, INetFwAuthorizedApplication::Enabled, INetFwAuthorizedApplication::get_Enabled, INetFwAuthorizedApplication::put_Enabled, ics.inetfwauthorizedapplication_enabled, netfw/INetFwAuthorizedApplication::Enabled, netfw/INetFwAuthorizedApplication::get_Enabled, netfw/INetFwAuthorizedApplication::put_Enabled, put_Enabled
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
 - INetFwAuthorizedApplication::put_Enabled
 - netfw/INetFwAuthorizedApplication::put_Enabled
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
 - INetFwAuthorizedApplication.Enabled
 - INetFwAuthorizedApplication.get_Enabled
 - INetFwAuthorizedApplication.put_Enabled
---

# INetFwAuthorizedApplication::put_Enabled


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether the settings for this application are currently enabled.

This property is read/write.

## -parameters

## -remarks

This property can be set to false (<b>VARIANT_FALSE</b>) to allow application  settings to be stored in the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications">INetFWAuthorizedApplications</a> collection without actually authorizing the application. 

The default value is true (<b>VARIANT_TRUE</b>) for new applications.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications">INetFWAuthorizedApplications</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplication">INetFwAuthorizedApplication</a>
