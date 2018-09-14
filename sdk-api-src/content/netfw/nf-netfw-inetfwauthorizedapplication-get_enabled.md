---
UID: NF:netfw.INetFwAuthorizedApplication.get_Enabled
title: INetFwAuthorizedApplication::get_Enabled
author: windows-sdk-content
description: Indicates whether the settings for this application are currently enabled.
old-location: ics\inetfwauthorizedapplication_enabled.htm
tech.root: ICS
ms.assetid: 03a1503e-aee5-484f-8a4c-a7e10dffe401
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Enabled property [ICS/ICF], Enabled property [ICS/ICF],INetFwAuthorizedApplication interface, INetFwAuthorizedApplication interface [ICS/ICF],Enabled property, INetFwAuthorizedApplication.Enabled, INetFwAuthorizedApplication.get_Enabled, INetFwAuthorizedApplication::Enabled, INetFwAuthorizedApplication::get_Enabled, INetFwAuthorizedApplication::put_Enabled, get_Enabled, ics.inetfwauthorizedapplication_enabled, netfw/INetFwAuthorizedApplication::Enabled, netfw/INetFwAuthorizedApplication::get_Enabled, netfw/INetFwAuthorizedApplication::put_Enabled
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
 - INetFwAuthorizedApplication.Enabled
 - INetFwAuthorizedApplication.get_Enabled
 - INetFwAuthorizedApplication.put_Enabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwAuthorizedApplication::get_Enabled


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether the settings for this application are currently enabled.

This property is read/write.


## -parameters


## -remarks



This property can be set to false (<b>VARIANT_FALSE</b>) to allow application  settings to be stored in the <a href="https://msdn.microsoft.com/70ea2cd1-5422-4db1-ab84-9924dab5623d">INetFWAuthorizedApplications</a> collection without actually authorizing the application. 

The default value is true (<b>VARIANT_TRUE</b>) for new applications.




## -see-also




<a href="https://msdn.microsoft.com/70ea2cd1-5422-4db1-ab84-9924dab5623d">INetFWAuthorizedApplications</a>



<a href="https://msdn.microsoft.com/1ddeeab8-b81b-4d34-9ca6-103147fb3426">INetFwAuthorizedApplication</a>
 

 

