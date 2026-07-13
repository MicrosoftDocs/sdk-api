---
UID: NF:netfw.INetFwRule.put_Name
title: INetFwRule::put_Name (netfw.h)
description: Specifies the friendly name of this rule. (Put)
helpviewer_keywords: ["INetFwRule interface [ICS/ICF]","Name property","INetFwRule.Name","INetFwRule.put_Name","INetFwRule::Name","INetFwRule::get_Name","INetFwRule::put_Name","Name property [ICS/ICF]","Name property [ICS/ICF]","INetFwRule interface","ics.inetfwrule_name","netfw/INetFwRule::Name","netfw/INetFwRule::get_Name","netfw/INetFwRule::put_Name","put_Name"]
old-location: ics\inetfwrule_name.htm
tech.root: ics
ms.assetid: 669ea684-5b00-4b60-8259-fad02cca572b
ms.date: 12/05/2018
ms.keywords: INetFwRule interface [ICS/ICF],Name property, INetFwRule.Name, INetFwRule.put_Name, INetFwRule::Name, INetFwRule::get_Name, INetFwRule::put_Name, Name property [ICS/ICF], Name property [ICS/ICF],INetFwRule interface, ics.inetfwrule_name, netfw/INetFwRule::Name, netfw/INetFwRule::get_Name, netfw/INetFwRule::put_Name, put_Name
req.header: netfw.h
req.include-header: 
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
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwRule::put_Name
 - netfw/INetFwRule::put_Name
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
 - INetFwRule.Name
 - INetFwRule.get_Name
 - INetFwRule.put_Name
---

# INetFwRule::put_Name


## -description

Specifies the friendly name of this rule.

This property is read/write.

## -parameters

## -remarks

This property is required. The string must not contain the "|" character.

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>
