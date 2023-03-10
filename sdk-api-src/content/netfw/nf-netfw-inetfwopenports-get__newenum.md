---
UID: NF:netfw.INetFwOpenPorts.get__NewEnum
title: INetFwOpenPorts::get__NewEnum (netfw.h)
description: Returns an object supporting IEnumVARIANT that can be used to iterate through all the ports in the collection.
helpviewer_keywords: ["INetFwOpenPorts interface [ICS/ICF]","_NewEnum property","INetFwOpenPorts._NewEnum","INetFwOpenPorts.get__NewEnum","INetFwOpenPorts::_NewEnum","INetFwOpenPorts::get__NewEnum","_NewEnum property [ICS/ICF]","_NewEnum property [ICS/ICF]","INetFwOpenPorts interface","get__NewEnum","ics.inetfwopenports_newenum","netfw/INetFwOpenPorts::_NewEnum","netfw/INetFwOpenPorts::get__NewEnum"]
old-location: ics\inetfwopenports_newenum.htm
tech.root: ics
ms.assetid: a7de2fef-7966-4742-a821-7fce0bf3bba2
ms.date: 12/05/2018
ms.keywords: INetFwOpenPorts interface [ICS/ICF],_NewEnum property, INetFwOpenPorts._NewEnum, INetFwOpenPorts.get__NewEnum, INetFwOpenPorts::_NewEnum, INetFwOpenPorts::get__NewEnum, _NewEnum property [ICS/ICF], _NewEnum property [ICS/ICF],INetFwOpenPorts interface, get__NewEnum, ics.inetfwopenports_newenum, netfw/INetFwOpenPorts::_NewEnum, netfw/INetFwOpenPorts::get__NewEnum
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
 - INetFwOpenPorts::get__NewEnum
 - netfw/INetFwOpenPorts::get__NewEnum
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
 - INetFwOpenPorts._NewEnum
 - INetFwOpenPorts.get__NewEnum
---

# INetFwOpenPorts::get__NewEnum


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Returns an object supporting <b>IEnumVARIANT</b> that can be used to iterate through all the ports in the collection.

Iteration through a collection is done using the <b>for each</b> construct in VBScript. See <a href="/previous-versions/windows/desktop/ics/iterating-a-collection">Iterating a Collection</a> for an example.

This property is read-only.

## -parameters

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenports">INetFwOpenPorts</a>



<a href="/previous-versions/windows/desktop/ics/iterating-a-collection">Iterating a Collection</a>