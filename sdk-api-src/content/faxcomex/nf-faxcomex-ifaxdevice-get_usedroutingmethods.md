---
UID: NF:faxcomex.IFaxDevice.get_UsedRoutingMethods
title: IFaxDevice::get_UsedRoutingMethods (faxcomex.h)
author: windows-sdk-content
description: The IFaxDevice::get_UsedRoutingMethods property is an array of strings that contains the GUIDs associated with the routing methods that the device uses, where each GUID represents an inbound routing method (FaxInboundRoutingMethod).
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_usedroutingmethods_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_650z.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxDevice interface [Fax Service],UsedRoutingMethods property, IFaxDevice.UsedRoutingMethods, IFaxDevice.get_UsedRoutingMethods, IFaxDevice::UsedRoutingMethods, IFaxDevice::get_UsedRoutingMethods, UsedRoutingMethods property [Fax Service], UsedRoutingMethods property [Fax Service],IFaxDevice interface, _mfax_faxdevice.usedroutingmethods, fax._mfax_faxdevice_cpp_mfax_faxdevice_usedroutingmethods_cpp, fax._mfax_faxdevice_usedroutingmethods, faxcomex/IFaxDevice::UsedRoutingMethods, faxcomex/IFaxDevice::get_UsedRoutingMethods, get_UsedRoutingMethods
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
 - IFaxDevice.UsedRoutingMethods
 - IFaxDevice.get_UsedRoutingMethods
 - IFaxDevice.get_UsedRoutingMethods
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxDevice::get_UsedRoutingMethods


## -description


The <b>IFaxDevice::get_UsedRoutingMethods</b> property is an array of strings that contains the GUIDs associated with the routing methods that the device uses, where each GUID represents an inbound routing method (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod">FaxInboundRoutingMethod</a>).

This property is read-only.


## -parameters


## -remarks



To add a routing method to or remove a routing method from the array of routing method GUIDs, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdevice-useroutingmethod-vb">IFaxDevice::UseRoutingMethod</a> method.

To read this property, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevice">IFaxDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdevice-useroutingmethod-vb">IFaxDevice::UseRoutingMethod</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-managing-the-fax-device-collection">Visual Basic Example</a>
 

 

