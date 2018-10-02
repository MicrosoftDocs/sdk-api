---
UID: NN:faxcomex.IFaxOutboundRoutingGroup
title: IFaxOutboundRoutingGroup
author: windows-sdk-content
description: The IFaxOutboundRoutingGroup interface describes a configuration object that is used by a fax client application to retrieve information about an individual fax outbound routing group.
old-location: fax\_mfax_faxoutboundroutinggroup_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_45o0_cpp.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFaxOutboundRoutingGroup, IFaxOutboundRoutingGroup interface [Fax Service], IFaxOutboundRoutingGroup interface [Fax Service],described, _mfax_faxoutboundroutinggroup_cpp, fax._mfax_faxoutboundroutinggroup_cpp, faxcomex/IFaxOutboundRoutingGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IFaxOutboundRoutingGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutboundRoutingGroup interface


## -description


The <b>IFaxOutboundRoutingGroup</b> interface describes a configuration object that is used by a fax client application to retrieve information about an individual fax outbound routing group. The object also includes a method to retrieve the ordered collection of device IDs (<a href="https://msdn.microsoft.com/en-us/library/ms686503(v=VS.85).aspx">IFaxDeviceIds</a> interfaces) that participate in the routing group. The order of the devices in the collection determines the relative order in which available devices send outgoing transmissions.
		


## -remarks



A default implementation of <b>IFaxOutboundRoutingGroup</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms689098(v=VS.85).aspx">FaxOutboundRoutingGroup</a> object.



