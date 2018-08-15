---
UID: NF:netfw.INetFwPolicy2.put_NotificationsDisabled
title: INetFwPolicy2::put_NotificationsDisabled
author: windows-sdk-content
description: Indicates whether interactive firewall notifications are disabled.
old-location: ics\inetfwpolicy2_notificationsdisabled.htm
old-project: ics
ms.assetid: 490442a4-3b60-4891-9d0e-71f8d2147999
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INetFwPolicy2 interface [ICS/ICF],NotificationsDisabled property, INetFwPolicy2.NotificationsDisabled, INetFwPolicy2.put_NotificationsDisabled, INetFwPolicy2::NotificationsDisabled, INetFwPolicy2::get_NotificationsDisabled, INetFwPolicy2::put_NotificationsDisabled, NotificationsDisabled property [ICS/ICF], NotificationsDisabled property [ICS/ICF],INetFwPolicy2 interface, ics.inetfwpolicy2_notificationsdisabled, netfw/INetFwPolicy2::NotificationsDisabled, netfw/INetFwPolicy2::get_NotificationsDisabled, netfw/INetFwPolicy2::put_NotificationsDisabled, put_NotificationsDisabled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netfw.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: NETISO_ERROR_TYPE
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
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwPolicy2::put_NotificationsDisabled


## -description


Indicates whether interactive firewall notifications are disabled.

This property is read/write.


## -parameters


## -remarks



When you pass a profile type obtained from the <a href="https://msdn.microsoft.com/93f4b508-30db-45a9-a7aa-df4a993dc50b">CurrentProfileTypes</a> property, make sure that you pass only one profile type to <b>get_NotificationsDisabled</b> and <b>put_NotificationsDisabled</b>. Note that <b>get_CurrentProfileTypes</b> can return multiple profiles.




## -see-also




<a href="https://msdn.microsoft.com/ef01a531-ddb0-4eb4-894b-82f613016396">INetFwPolicy2</a>
 

 

