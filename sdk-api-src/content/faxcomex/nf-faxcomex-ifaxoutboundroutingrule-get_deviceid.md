---
UID: NF:faxcomex.IFaxOutboundRoutingRule.get_DeviceId
title: IFaxOutboundRoutingRule::get_DeviceId (faxcomex.h)
description: The IFaxOutboundRoutingRule::get_DeviceId property specifies the device ID if the outbound routing rule points to a single fax device. (Get)
helpviewer_keywords: ["DeviceId property [Fax Service]","DeviceId property [Fax Service]","IFaxOutboundRoutingRule interface","IFaxOutboundRoutingRule interface [Fax Service]","DeviceId property","IFaxOutboundRoutingRule.DeviceId","IFaxOutboundRoutingRule.get_DeviceId","IFaxOutboundRoutingRule.put_DeviceId","IFaxOutboundRoutingRule::DeviceId","IFaxOutboundRoutingRule::get_DeviceId","IFaxOutboundRoutingRule::put_DeviceId","_mfax_faxoutboundroutingrule.deviceid","fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_deviceid_cpp","fax._mfax_faxoutboundroutingrule_deviceid","faxcomex/IFaxOutboundRoutingRule::DeviceId","faxcomex/IFaxOutboundRoutingRule::get_DeviceId","faxcomex/IFaxOutboundRoutingRule::put_DeviceId","get_DeviceId"]
old-location: fax\_mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_deviceid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6pwk.htm
ms.date: 12/05/2018
ms.keywords: DeviceId property [Fax Service], DeviceId property [Fax Service],IFaxOutboundRoutingRule interface, IFaxOutboundRoutingRule interface [Fax Service],DeviceId property, IFaxOutboundRoutingRule.DeviceId, IFaxOutboundRoutingRule.get_DeviceId, IFaxOutboundRoutingRule.put_DeviceId, IFaxOutboundRoutingRule::DeviceId, IFaxOutboundRoutingRule::get_DeviceId, IFaxOutboundRoutingRule::put_DeviceId, _mfax_faxoutboundroutingrule.deviceid, fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_deviceid_cpp, fax._mfax_faxoutboundroutingrule_deviceid, faxcomex/IFaxOutboundRoutingRule::DeviceId, faxcomex/IFaxOutboundRoutingRule::get_DeviceId, faxcomex/IFaxOutboundRoutingRule::put_DeviceId, get_DeviceId
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
 - IFaxOutboundRoutingRule::get_DeviceId
 - faxcomex/IFaxOutboundRoutingRule::get_DeviceId
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
 - IFaxOutboundRoutingRule.DeviceId
 - IFaxOutboundRoutingRule.get_DeviceId
 - IFaxOutboundRoutingRule.put_DeviceId
 - IFaxOutboundRoutingRule.get_DeviceId
 - IFaxOutboundRoutingRule.put_DeviceId
---

# IFaxOutboundRoutingRule::get_DeviceId


## -description

The <b>IFaxOutboundRoutingRule::get_DeviceId</b> property specifies the device ID if the outbound routing rule points to a single fax device.

This property is read/write.

## -parameters

## -remarks

This property is valid only if the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule-usedevice-vb">IFaxOutboundRoutingRule::get_UseDevice</a> property is equal to <b>TRUE</b>.

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a>
