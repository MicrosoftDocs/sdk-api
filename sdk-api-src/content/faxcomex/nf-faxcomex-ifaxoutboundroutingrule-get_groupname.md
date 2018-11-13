---
UID: NF:faxcomex.IFaxOutboundRoutingRule.get_GroupName
title: IFaxOutboundRoutingRule::get_GroupName
author: windows-sdk-content
description: The IFaxOutboundRoutingRule::get_GroupName property specifies the group name if the outbound routing rule points to a group of fax devices.
old-location: fax\_mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_groupname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_2x0l.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: GroupName property [Fax Service], GroupName property [Fax Service],IFaxOutboundRoutingRule interface, IFaxOutboundRoutingRule interface [Fax Service],GroupName property, IFaxOutboundRoutingRule.GroupName, IFaxOutboundRoutingRule.get_GroupName, IFaxOutboundRoutingRule.put_GroupName, IFaxOutboundRoutingRule::GroupName, IFaxOutboundRoutingRule::get_GroupName, IFaxOutboundRoutingRule::put_GroupName, _mfax_faxoutboundroutingrule.groupname, fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_groupname_cpp, fax._mfax_faxoutboundroutingrule_groupname, faxcomex/IFaxOutboundRoutingRule::GroupName, faxcomex/IFaxOutboundRoutingRule::get_GroupName, faxcomex/IFaxOutboundRoutingRule::put_GroupName, get_GroupName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutboundRoutingRule::get_GroupName


## -description


The <b>IFaxOutboundRoutingRule::get_GroupName</b> property specifies the group name if the outbound routing rule points to a group of fax devices.

This property is read/write.


## -parameters


## -remarks



This property is valid only if the <a href="https://msdn.microsoft.com/64b1778a-a53f-468b-8ec0-93db23036730">IFaxOutboundRoutingRule::get_UseDevice</a> property is equal to <b>FALSE</b>.

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a>



<a href="https://msdn.microsoft.com/29b577f6-6aeb-43fd-8a0f-657ef1c16999">IFaxOutboundRoutingRule</a>



<a href="https://msdn.microsoft.com/35bb803d-fce4-46a3-825a-ec3a5138ed67">Visual Basic Example</a>
 

 

