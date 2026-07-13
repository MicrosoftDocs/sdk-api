---
UID: NF:netfw.INetFwRule.put_Description
title: INetFwRule::put_Description (netfw.h)
description: Specifies the description of this rule. (Put)
helpviewer_keywords: ["Description property [ICS/ICF]","Description property [ICS/ICF]","INetFwRule interface","INetFwRule interface [ICS/ICF]","Description property","INetFwRule.Description","INetFwRule.put_Description","INetFwRule::Description","INetFwRule::get_Description","INetFwRule::put_Description","ics.inetfwrule_description","netfw/INetFwRule::Description","netfw/INetFwRule::get_Description","netfw/INetFwRule::put_Description","put_Description"]
old-location: ics\inetfwrule_description.htm
tech.root: ics
ms.assetid: 47e5a5ff-d8a7-46e6-aa42-b9e7d544954b
ms.date: 12/05/2018
ms.keywords: Description property [ICS/ICF], Description property [ICS/ICF],INetFwRule interface, INetFwRule interface [ICS/ICF],Description property, INetFwRule.Description, INetFwRule.put_Description, INetFwRule::Description, INetFwRule::get_Description, INetFwRule::put_Description, ics.inetfwrule_description, netfw/INetFwRule::Description, netfw/INetFwRule::get_Description, netfw/INetFwRule::put_Description, put_Description
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
 - INetFwRule::put_Description
 - netfw/INetFwRule::put_Description
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
 - INetFwRule.Description
 - INetFwRule.get_Description
 - INetFwRule.put_Description
---

# INetFwRule::put_Description


## -description

Specifies the description of this rule.

This property is read/write.

## -parameters

## -remarks

This property is optional. The string must not contain the "|" character.

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>
