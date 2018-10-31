---
UID: NF:faxcom.IFaxPort.get_CanModify
title: IFaxPort::get_CanModify
author: windows-sdk-content
description: The IFaxPort::get_CanModify property is a Boolean value that indicates whether the user has permission to modify configuration information for the fax port.
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_canmodify_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_920p.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CanModify property [Fax Service], CanModify property [Fax Service],IFaxPort interface, IFaxPort interface [Fax Service],CanModify property, IFaxPort.CanModify, IFaxPort.get_CanModify, IFaxPort::CanModify, IFaxPort::get_CanModify, _mfax_ifaxport_get_canmodify, fax._mfax_ifaxport_get_canmodify, fax._mfax_ifaxport_mfax_ifaxport_get_canmodify_cpp, faxcom/IFaxPort::CanModify, faxcom/IFaxPort::get_CanModify, get_CanModify
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
 - IFaxPort.CanModify
 - IFaxPort.get_CanModify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxPort::get_CanModify


## -description


The <b>IFaxPort::get_CanModify</b> property is a Boolean value that indicates whether the user has permission to modify configuration information for the fax port.

This property is read-only.


## -parameters


## -remarks



To ensure that the client has permission to modify the specified fax port, a fax client application can call the <b>IFaxPort::get_CanModify</b> property before calling any method that begins with <b>IFaxPort::put_</b>. For more information, see <a href="https://msdn.microsoft.com/784fdc0e-c664-4ea9-8a4f-0a0cd89c0d81">Fax Device Management</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>
 

 

