---
UID: NF:faxcom.IFaxRoutingMethod.get_Enable
title: IFaxRoutingMethod::get_Enable
author: windows-sdk-content
description: The IFaxRoutingMethod::get_Enable property is a Boolean value that indicates whether a fax routing method is enabled on a particular fax port.
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_enable_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1vmt.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: Enable property [Fax Service], Enable property [Fax Service],IFaxRoutingMethod interface, IFaxRoutingMethod interface [Fax Service],Enable property, IFaxRoutingMethod.Enable, IFaxRoutingMethod.get_Enable, IFaxRoutingMethod::Enable, IFaxRoutingMethod::get_Enable, IFaxRoutingMethod::put_Enable, _mfax_ifaxroutingmethod_get_enable, fax._mfax_ifaxroutingmethod_get_enable, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_enable_cpp, faxcom/IFaxRoutingMethod::Enable, faxcom/IFaxRoutingMethod::get_Enable, faxcom/IFaxRoutingMethod::put_Enable, get_Enable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxRoutingMethod.Enable
 - IFaxRoutingMethod.get_Enable
 - IFaxRoutingMethod.put_Enable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethod::get_Enable


## -description


The <b>IFaxRoutingMethod::get_Enable</b> property is a Boolean value that indicates whether a fax routing method is enabled on a particular fax port.


This property is read/write.


## -parameters


## -remarks



If a fax client application passes a value of <b>TRUE</b> to the <b>IFaxRoutingMethod::get_Enable</b> property, the property enables the routing method for inbound faxes on the parent port.




## -see-also




<a href="https://msdn.microsoft.com/b09b6e5f-fa1d-4d0b-8581-e0ba779b72bb">CanModify</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

