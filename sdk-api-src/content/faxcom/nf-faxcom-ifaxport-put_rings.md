---
UID: NF:faxcom.IFaxPort.put_Rings
title: IFaxPort::put_Rings
author: windows-sdk-content
description: The IFaxPort::get_Rings property represents the number of rings an incoming fax call should wait before the fax port answers the call.
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_rings_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3jjn.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxPort interface [Fax Service],Rings property, IFaxPort.Rings, IFaxPort.put_Rings, IFaxPort::Rings, IFaxPort::get_Rings, IFaxPort::put_Rings, Rings property [Fax Service], Rings property [Fax Service],IFaxPort interface, _mfax_ifaxport_get_rings, fax._mfax_ifaxport_get_rings, fax._mfax_ifaxport_mfax_ifaxport_get_rings_cpp, faxcom/IFaxPort::Rings, faxcom/IFaxPort::get_Rings, faxcom/IFaxPort::put_Rings, put_Rings
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
 - IFaxPort.Rings
 - IFaxPort.get_Rings
 - IFaxPort.put_Rings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcom.h
: 
- IFaxPort.put_Rings
: 
---

# IFaxPort::put_Rings


## -description


The <b>IFaxPort::get_Rings</b> property represents the number of rings an incoming fax call should wait before the fax port answers the call. 

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="https://msdn.microsoft.com/b09b6e5f-fa1d-4d0b-8581-e0ba779b72bb">IFaxPort::get_CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
The fax server ignores the <b>IFaxPort::get_Rings</b> property unless the specified fax port is enabled to receive faxes.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>
 

 

