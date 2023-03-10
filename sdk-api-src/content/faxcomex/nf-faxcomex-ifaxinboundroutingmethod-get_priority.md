---
UID: NF:faxcomex.IFaxInboundRoutingMethod.get_Priority
title: IFaxInboundRoutingMethod::get_Priority (faxcomex.h)
description: The Priority property is a value associated with the order in which the fax service calls the routing method when the service receives a fax job. (Get)
helpviewer_keywords: ["IFaxInboundRoutingMethod interface [Fax Service]","Priority property","IFaxInboundRoutingMethod.Priority","IFaxInboundRoutingMethod.get_Priority","IFaxInboundRoutingMethod::Priority","IFaxInboundRoutingMethod::get_Priority","IFaxInboundRoutingMethod::put_Priority","Priority property [Fax Service]","Priority property [Fax Service]","IFaxInboundRoutingMethod interface","_mfax_faxinboundroutingmethod.priority_cpp","fax._mfax_faxinboundroutingmethod_priority_cpp","faxcomex/IFaxInboundRoutingMethod::Priority","faxcomex/IFaxInboundRoutingMethod::get_Priority","faxcomex/IFaxInboundRoutingMethod::put_Priority","get_Priority"]
old-location: fax\_mfax_faxinboundroutingmethod_priority_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4kqh_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxInboundRoutingMethod interface [Fax Service],Priority property, IFaxInboundRoutingMethod.Priority, IFaxInboundRoutingMethod.get_Priority, IFaxInboundRoutingMethod::Priority, IFaxInboundRoutingMethod::get_Priority, IFaxInboundRoutingMethod::put_Priority, Priority property [Fax Service], Priority property [Fax Service],IFaxInboundRoutingMethod interface, _mfax_faxinboundroutingmethod.priority_cpp, fax._mfax_faxinboundroutingmethod_priority_cpp, faxcomex/IFaxInboundRoutingMethod::Priority, faxcomex/IFaxInboundRoutingMethod::get_Priority, faxcomex/IFaxInboundRoutingMethod::put_Priority, get_Priority
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
 - IFaxInboundRoutingMethod::get_Priority
 - faxcomex/IFaxInboundRoutingMethod::get_Priority
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
 - IFaxInboundRoutingMethod.Priority
 - IFaxInboundRoutingMethod.get_Priority
 - IFaxInboundRoutingMethod.put_Priority
---

# IFaxInboundRoutingMethod::get_Priority


## -description

The <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-priority">Priority</a> property is a value associated with the order in which the fax service calls the routing method when the service receives a fax job.

This property is read/write.

## -parameters

## -remarks

Valid values for this property are 1 through <i>n</i>, where 1 is the highest priority.

You should assign a unique priority value to each routing method. After you call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-save-vb">IFaxInboundRoutingMethod::Save</a> method, the fax service sorts the routing methods by priority. If two routing methods have the same priority, the fax service will choose which will have a higher priority.

If you want a particular routing method to have the lowest possible priority, specify a very large value, such as 999999, and then call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-save-vb">IFaxInboundRoutingMethod::Save</a> method.

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod">FaxInboundRoutingMethod</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingmethod">IFaxInboundRoutingMethod</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-routing-extensions-and-routing-methods">Visual Basic Example</a>
