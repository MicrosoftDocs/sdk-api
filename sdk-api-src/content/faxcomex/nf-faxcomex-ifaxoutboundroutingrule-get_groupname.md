---
UID: NF:faxcomex.IFaxOutboundRoutingRule.get_GroupName
title: IFaxOutboundRoutingRule::get_GroupName (faxcomex.h)
description: The IFaxOutboundRoutingRule::get_GroupName property specifies the group name if the outbound routing rule points to a group of fax devices. (Get)
helpviewer_keywords: ["GroupName property [Fax Service]","GroupName property [Fax Service]","IFaxOutboundRoutingRule interface","IFaxOutboundRoutingRule interface [Fax Service]","GroupName property","IFaxOutboundRoutingRule.GroupName","IFaxOutboundRoutingRule.get_GroupName","IFaxOutboundRoutingRule.put_GroupName","IFaxOutboundRoutingRule::GroupName","IFaxOutboundRoutingRule::get_GroupName","IFaxOutboundRoutingRule::put_GroupName","_mfax_faxoutboundroutingrule.groupname","fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_groupname_cpp","fax._mfax_faxoutboundroutingrule_groupname","faxcomex/IFaxOutboundRoutingRule::GroupName","faxcomex/IFaxOutboundRoutingRule::get_GroupName","faxcomex/IFaxOutboundRoutingRule::put_GroupName","get_GroupName"]
old-location: fax\_mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_groupname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_2x0l.htm
ms.date: 12/05/2018
ms.keywords: GroupName property [Fax Service], GroupName property [Fax Service],IFaxOutboundRoutingRule interface, IFaxOutboundRoutingRule interface [Fax Service],GroupName property, IFaxOutboundRoutingRule.GroupName, IFaxOutboundRoutingRule.get_GroupName, IFaxOutboundRoutingRule.put_GroupName, IFaxOutboundRoutingRule::GroupName, IFaxOutboundRoutingRule::get_GroupName, IFaxOutboundRoutingRule::put_GroupName, _mfax_faxoutboundroutingrule.groupname, fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_groupname_cpp, fax._mfax_faxoutboundroutingrule_groupname, faxcomex/IFaxOutboundRoutingRule::GroupName, faxcomex/IFaxOutboundRoutingRule::get_GroupName, faxcomex/IFaxOutboundRoutingRule::put_GroupName, get_GroupName
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxOutboundRoutingRule::get_GroupName
 - faxcomex/IFaxOutboundRoutingRule::get_GroupName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutboundRoutingRule.GroupName
 - IFaxOutboundRoutingRule.get_GroupName
 - IFaxOutboundRoutingRule.put_GroupName
 - IFaxOutboundRoutingRule.get_GroupName
 - IFaxOutboundRoutingRule.put_GroupName
---

# IFaxOutboundRoutingRule::get_GroupName


## -description

The <b>IFaxOutboundRoutingRule::get_GroupName</b> property specifies the group name if the outbound routing rule points to a group of fax devices.

This property is read/write.

## -parameters

## -remarks

This property is valid only if the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule-usedevice-vb">IFaxOutboundRoutingRule::get_UseDevice</a> property is equal to <b>FALSE</b>.

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-creating-and-managing-outbound-routing-rules">Visual Basic Example</a>
