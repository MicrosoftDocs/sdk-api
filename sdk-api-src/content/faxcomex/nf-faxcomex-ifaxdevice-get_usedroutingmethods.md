---
UID: NF:faxcomex.IFaxDevice.get_UsedRoutingMethods
title: IFaxDevice::get_UsedRoutingMethods
author: windows-sdk-content
description: The IFaxDevice::get_UsedRoutingMethods property is an array of strings that contains the GUIDs associated with the routing methods that the device uses, where each GUID represents an inbound routing method (FaxInboundRoutingMethod).
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_usedroutingmethods_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_650z.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxDevice interface [Fax Service],UsedRoutingMethods property, IFaxDevice.UsedRoutingMethods, IFaxDevice.get_UsedRoutingMethods, IFaxDevice::UsedRoutingMethods, IFaxDevice::get_UsedRoutingMethods, UsedRoutingMethods property [Fax Service], UsedRoutingMethods property [Fax Service],IFaxDevice interface, _mfax_faxdevice.usedroutingmethods, fax._mfax_faxdevice_cpp_mfax_faxdevice_usedroutingmethods_cpp, fax._mfax_faxdevice_usedroutingmethods, faxcomex/IFaxDevice::UsedRoutingMethods, faxcomex/IFaxDevice::get_UsedRoutingMethods, get_UsedRoutingMethods
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
 - IFaxDevice.UsedRoutingMethods
 - IFaxDevice.get_UsedRoutingMethods
 - IFaxDevice.get_UsedRoutingMethods
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDevice::get_UsedRoutingMethods


## -description


The <b>IFaxDevice::get_UsedRoutingMethods</b> property is an array of strings that contains the GUIDs associated with the routing methods that the device uses, where each GUID represents an inbound routing method (<a href="https://msdn.microsoft.com/8eb68201-4c87-41ce-a401-a039b5ad454d">FaxInboundRoutingMethod</a>).

This property is read-only.


## -parameters


## -remarks



To add a routing method to or remove a routing method from the array of routing method GUIDs, call the <a href="https://msdn.microsoft.com/fcfe525b-6478-4202-839c-8ba984965bdb">IFaxDevice::UseRoutingMethod</a> method.

To read this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a>



<a href="https://msdn.microsoft.com/3f4f4e83-df62-43af-903c-0b816bade3b9">IFaxDevice</a>



<a href="https://msdn.microsoft.com/fcfe525b-6478-4202-839c-8ba984965bdb">IFaxDevice::UseRoutingMethod</a>



<a href="https://msdn.microsoft.com/8e0d5b13-2126-49a2-80b7-ae3a817496bd">Visual Basic Example</a>
 

 

