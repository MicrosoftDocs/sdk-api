---
UID: NF:netfw.INetFwRule3.put_LocalUserOwner
title: INetFwRule3::put_LocalUserOwner
author: windows-sdk-content
description: Specifies the user security identifier (SID) of the user who is the owner of the rule.
old-location: ics\inetfwrule3_localuserowner.htm
old-project: ics
ms.assetid: 5eeacde4-6e25-49dc-a8f5-77a6e56dcade
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INetFwRule3 interface [ICS/ICF],LocalUserOwner property, INetFwRule3.LocalUserOwner, INetFwRule3.put_LocalUserOwner, INetFwRule3::LocalUserOwner, INetFwRule3::get_LocalUserOwner, INetFwRule3::put_LocalUserOwner, LocalUserOwner property [ICS/ICF], LocalUserOwner property [ICS/ICF],INetFwRule3 interface, ics.inetfwrule3_localuserowner, netfw/INetFwRule3::LocalUserOwner, netfw/INetFwRule3::get_LocalUserOwner, netfw/INetFwRule3::put_LocalUserOwner, put_LocalUserOwner
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netfw.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - INetFwRule3.LocalUserOwner
 - INetFwRule3.get_LocalUserOwner
 - INetFwRule3.put_LocalUserOwner
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwRule3::put_LocalUserOwner


## -description


Specifies the user security identifier (SID) of the user who is the owner of the rule. 

This property is read/write.


## -parameters


## -remarks



If this rule does not specify <b>localUserConditions</b>, all the traffic that this rule matches must be destined to or originated from this user.




## -see-also




<a href="https://msdn.microsoft.com/72bf5ac3-7ee7-4837-96b2-815b499aac2f">INetFwRule3</a>
 

 

