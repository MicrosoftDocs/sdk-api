---
UID: NF:netfw.INetFwOpenPorts.get__NewEnum
title: INetFwOpenPorts::get__NewEnum
author: windows-sdk-content
description: Returns an object supporting IEnumVARIANT that can be used to iterate through all the ports in the collection.
old-location: ics\inetfwopenports_newenum.htm
tech.root: ICS
ms.assetid: a7de2fef-7966-4742-a821-7fce0bf3bba2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: INetFwOpenPorts interface [ICS/ICF],_NewEnum property, INetFwOpenPorts._NewEnum, INetFwOpenPorts.get__NewEnum, INetFwOpenPorts::_NewEnum, INetFwOpenPorts::get__NewEnum, _NewEnum property [ICS/ICF], _NewEnum property [ICS/ICF],INetFwOpenPorts interface, get__NewEnum, ics.inetfwopenports_newenum, netfw/INetFwOpenPorts::_NewEnum, netfw/INetFwOpenPorts::get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwOpenPorts::get__NewEnum


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Returns an object supporting <b>IEnumVARIANT</b> that can be used to iterate through all the ports in the collection.

Iteration through a collection is done using the <b>for each</b> construct in VBScript. See <a href="https://msdn.microsoft.com/2a502415-c12a-4d07-9f72-a3967e87d37d">Iterating a Collection</a> for an example.

This property is read-only.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/a3a6e5c1-5818-419c-8df4-966b2fbcd8c0">INetFwOpenPorts</a>



<a href="https://msdn.microsoft.com/2a502415-c12a-4d07-9f72-a3967e87d37d">Iterating a Collection</a>
 

 

