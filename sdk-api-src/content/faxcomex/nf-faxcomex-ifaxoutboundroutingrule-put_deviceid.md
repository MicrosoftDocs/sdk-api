---
UID: NF:faxcomex.IFaxOutboundRoutingRule.put_DeviceId
title: IFaxOutboundRoutingRule::put_DeviceId (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutboundRoutingRule::get_DeviceId property specifies the device ID if the outbound routing rule points to a single fax device.
old-location: fax\_mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_deviceid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6pwk.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeviceId property [Fax Service], DeviceId property [Fax Service],IFaxOutboundRoutingRule interface, IFaxOutboundRoutingRule interface [Fax Service],DeviceId property, IFaxOutboundRoutingRule.DeviceId, IFaxOutboundRoutingRule.get_DeviceId, IFaxOutboundRoutingRule.put_DeviceId, IFaxOutboundRoutingRule::DeviceId, IFaxOutboundRoutingRule::get_DeviceId, IFaxOutboundRoutingRule::put_DeviceId, _mfax_faxoutboundroutingrule.deviceid, fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_deviceid_cpp, fax._mfax_faxoutboundroutingrule_deviceid, faxcomex/IFaxOutboundRoutingRule::DeviceId, faxcomex/IFaxOutboundRoutingRule::get_DeviceId, faxcomex/IFaxOutboundRoutingRule::put_DeviceId, put_DeviceId
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
 - IFaxOutboundRoutingRule.DeviceId
 - IFaxOutboundRoutingRule.get_DeviceId
 - IFaxOutboundRoutingRule.put_DeviceId
 - IFaxOutboundRoutingRule.get_DeviceId
 - IFaxOutboundRoutingRule.put_DeviceId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutboundRoutingRule::put_DeviceId


## -description


The <b>IFaxOutboundRoutingRule::get_DeviceId</b> property specifies the device ID if the outbound routing rule points to a single fax device.

This property is read/write.


## -parameters


## -remarks



This property is valid only if the <a href="https://msdn.microsoft.com/en-us/library/ms688614(v=VS.85).aspx">IFaxOutboundRoutingRule::get_UseDevice</a> property is equal to <b>TRUE</b>.

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690230(v=VS.85).aspx">FaxOutboundRoutingRule</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690232(v=VS.85).aspx">IFaxOutboundRoutingRule</a>
 

 

