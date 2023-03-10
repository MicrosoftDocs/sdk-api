---
UID: NN:netfw.INetFwMgr
title: INetFwMgr (netfw.h)
description: The INetFwMgr interface provides access to the firewall settings for a computer.
helpviewer_keywords: ["INetFwMgr","INetFwMgr interface [ICS/ICF]","INetFwMgr interface [ICS/ICF]","described","ics.inetfwmgr","netfw/INetFwMgr"]
old-location: ics\inetfwmgr.htm
tech.root: ics
ms.assetid: 7534ea10-7553-4ec2-af68-0b0393ffc003
ms.date: 12/05/2018
ms.keywords: INetFwMgr, INetFwMgr interface [ICS/ICF], INetFwMgr interface [ICS/ICF],described, ics.inetfwmgr, netfw/INetFwMgr
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
 - INetFwMgr
 - netfw/INetFwMgr
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
 - INetFwMgr
---

# INetFwMgr interface


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwservices">INetFwMgr</a> interface  provides access to the firewall settings for a computer.

## -inheritance

The <b>INetFwMgr</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwMgr</b> also has these types of members:

## -remarks

<b>Windows Vista:  </b>Windows Vista users must use applications developed in Windows Vista for all methods and properties of this interface.

This interface is
supported by the HNetCfg.FwMgr COM object. 

All configuration changes take
effect immediately.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
