---
UID: NF:faxcom.IFaxPort.get_Name
title: IFaxPort::get_Name
author: windows-sdk-content
description: The IFaxPort::get_Name property is a null-terminated string that contains the user-friendly display name for a fax port.
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_name_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1ep1.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxPort interface [Fax Service],Name property, IFaxPort.Name, IFaxPort.get_Name, IFaxPort::Name, IFaxPort::get_Name, Name property [Fax Service], Name property [Fax Service],IFaxPort interface, _mfax_ifaxport_get_name, fax._mfax_ifaxport_get_name, fax._mfax_ifaxport_mfax_ifaxport_get_name_cpp, faxcom/IFaxPort::Name, faxcom/IFaxPort::get_Name, get_Name
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
 - IFaxPort.Name
 - IFaxPort.get_Name
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxPort::get_Name


## -description


The <b>IFaxPort::get_Name</b> property is a null-terminated string that contains the 
user-friendly display name for a fax port.

This property is read-only.


## -parameters


## -remarks



Note that it is possible for multiple fax ports to have the same user-friendly 
name. Use the <a href="https://msdn.microsoft.com/6909e37a-0a6c-475f-ab41-c2e1817349f5">IFaxPort::get_DeviceId</a> property to uniquely identify a fax port.

<b>IFaxPort::get_Name</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/6909e37a-0a6c-475f-ab41-c2e1817349f5">IFaxPort::get_DeviceId</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>
 

 

