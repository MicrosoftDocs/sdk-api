---
UID: NF:netfw.INetFwProfile.put_ExceptionsNotAllowed
title: INetFwProfile::put_ExceptionsNotAllowed (netfw.h)
author: windows-sdk-content
description: Indicates whether the firewall should not allow exceptions.
old-location: ics\inetfwprofile_exceptionsnotallowed.htm
tech.root: ics
ms.assetid: 5b9eae72-546e-4724-acba-c2f2d9ad1cc6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExceptionsNotAllowed property [ICS/ICF], ExceptionsNotAllowed property [ICS/ICF],INetFwProfile interface, INetFwProfile interface [ICS/ICF],ExceptionsNotAllowed property, INetFwProfile.ExceptionsNotAllowed, INetFwProfile.put_ExceptionsNotAllowed, INetFwProfile::ExceptionsNotAllowed, INetFwProfile::get_ExceptionsNotAllowed, INetFwProfile::put_ExceptionsNotAllowed, ics.inetfwprofile_exceptionsnotallowed, netfw/INetFwProfile::ExceptionsNotAllowed, netfw/INetFwProfile::get_ExceptionsNotAllowed, netfw/INetFwProfile::put_ExceptionsNotAllowed, put_ExceptionsNotAllowed
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
 - INetFwProfile.ExceptionsNotAllowed
 - INetFwProfile.get_ExceptionsNotAllowed
 - INetFwProfile.put_ExceptionsNotAllowed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwProfile::put_ExceptionsNotAllowed


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether the firewall should not allow exceptions.

This property is read/write.


## -parameters


## -remarks



All interfaces are firewalled. This means that all the exceptions; such as GloballyOpenPorts, Applications, or Services, which are  specified in the profile, are ignored
   and only locally initiated traffic is allowed.

 The resulting  firewall status is determined by the combination of  two levels: First check the global operation mode, then the mode on the interface of interest. Use the procedure <a href="https://msdn.microsoft.com/c2a6f57d-e05b-4143-90ad-39ca32d66c66">Checking the Effective Firewall Status</a> to determine the overall operational state. 




## -see-also




<a href="https://msdn.microsoft.com/694bbff5-003d-4dde-9a85-f81ca29e6208">INetFwProfile</a>
 

 

