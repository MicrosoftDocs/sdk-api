---
UID: NF:netfw.INetFwRule3.get_LocalUserOwner
title: INetFwRule3::get_LocalUserOwner (netfw.h)
description: Specifies the user security identifier (SID) of the user who is the owner of the rule. (Get)
helpviewer_keywords: ["INetFwRule3 interface [ICS/ICF]","LocalUserOwner property","INetFwRule3.LocalUserOwner","INetFwRule3.get_LocalUserOwner","INetFwRule3::LocalUserOwner","INetFwRule3::get_LocalUserOwner","INetFwRule3::put_LocalUserOwner","LocalUserOwner property [ICS/ICF]","LocalUserOwner property [ICS/ICF]","INetFwRule3 interface","get_LocalUserOwner","ics.inetfwrule3_localuserowner","netfw/INetFwRule3::LocalUserOwner","netfw/INetFwRule3::get_LocalUserOwner","netfw/INetFwRule3::put_LocalUserOwner"]
old-location: ics\inetfwrule3_localuserowner.htm
tech.root: ics
ms.assetid: 5eeacde4-6e25-49dc-a8f5-77a6e56dcade
ms.date: 12/05/2018
ms.keywords: INetFwRule3 interface [ICS/ICF],LocalUserOwner property, INetFwRule3.LocalUserOwner, INetFwRule3.get_LocalUserOwner, INetFwRule3::LocalUserOwner, INetFwRule3::get_LocalUserOwner, INetFwRule3::put_LocalUserOwner, LocalUserOwner property [ICS/ICF], LocalUserOwner property [ICS/ICF],INetFwRule3 interface, get_LocalUserOwner, ics.inetfwrule3_localuserowner, netfw/INetFwRule3::LocalUserOwner, netfw/INetFwRule3::get_LocalUserOwner, netfw/INetFwRule3::put_LocalUserOwner
req.header: netfw.h
req.include-header: 
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
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwRule3::get_LocalUserOwner
 - netfw/INetFwRule3::get_LocalUserOwner
dev_langs:
 - c++
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
---

# INetFwRule3::get_LocalUserOwner


## -description

Specifies the user security identifier (SID) of the user who is the owner of the rule. 

This property is read/write.

## -parameters

## -remarks

If this rule does not specify <b>localUserConditions</b>, all the traffic that this rule matches must be destined to or originated from this user.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule3">INetFwRule3</a>
