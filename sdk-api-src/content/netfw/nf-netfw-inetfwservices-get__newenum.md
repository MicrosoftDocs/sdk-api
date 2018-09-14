---
UID: NF:netfw.INetFwServices.get__NewEnum
title: INetFwServices::get__NewEnum
author: windows-sdk-content
description: Returns an object supporting IEnumVARIANT that can be used to iterate through all the services in the collection.
old-location: ics\inetfwservices_newenum.htm
tech.root: ICS
ms.assetid: 2da6560f-2eca-4391-88c1-a86948d19d58
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: INetFwServices interface [ICS/ICF],_NewEnum property, INetFwServices._NewEnum, INetFwServices.get__NewEnum, INetFwServices::_NewEnum, INetFwServices::get__NewEnum, _NewEnum property [ICS/ICF], _NewEnum property [ICS/ICF],INetFwServices interface, get__NewEnum, ics.inetfwservices_newenum, netfw/INetFwServices::_NewEnum, netfw/INetFwServices::get__NewEnum
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
 - INetFwServices._NewEnum
 - INetFwServices.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwServices::get__NewEnum


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Returns an object supporting <b>IEnumVARIANT</b> that can be used to iterate through all the services in the collection.

Iteration through a collection is done using the <b>for each</b> construct in VBScript. See <a href="https://msdn.microsoft.com/2a502415-c12a-4d07-9f72-a3967e87d37d">Iterating a Collection</a> for an example.

This property is read-only.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/b99464c5-dabc-405a-ad3e-da06a6faef47">INetFwServices</a>



<a href="https://msdn.microsoft.com/2a502415-c12a-4d07-9f72-a3967e87d37d">Iterating a Collection</a>
 

 

