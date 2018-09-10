---
UID: NF:faxcom.IFaxRoutingMethod.get_DeviceName
title: IFaxRoutingMethod::get_DeviceName
author: windows-sdk-content
description: The IFaxRoutingMethod::get_DeviceName property is a null-terminated string that contains the user-friendly display name for a fax port.
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_devicename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0tk5.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: DeviceName property [Fax Service], DeviceName property [Fax Service],IFaxRoutingMethod interface, IFaxRoutingMethod interface [Fax Service],DeviceName property, IFaxRoutingMethod.DeviceName, IFaxRoutingMethod.get_DeviceName, IFaxRoutingMethod::DeviceName, IFaxRoutingMethod::get_DeviceName, _mfax_ifaxroutingmethod_get_devicename, fax._mfax_ifaxroutingmethod_get_devicename, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_devicename_cpp, faxcom/IFaxRoutingMethod::DeviceName, faxcom/IFaxRoutingMethod::get_DeviceName, get_DeviceName
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
 - IFaxRoutingMethod.DeviceName
 - IFaxRoutingMethod.get_DeviceName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethod::get_DeviceName


## -description


The <b>IFaxRoutingMethod::get_DeviceName</b> property is a null-terminated string that contains the user-friendly display name for a fax port. 

This property is read-only.


## -parameters


## -remarks



Note that it is possible for multiple fax ports to have the same user-friendly name. You can use the <a href="https://msdn.microsoft.com/81ad011f-be41-49d8-bc43-2a42aa28fa2f">IFaxRoutingMethod::get_DeviceId</a> property to uniquely identify a fax port.

<b>IFaxRoutingMethod::get_DeviceName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/81ad011f-be41-49d8-bc43-2a42aa28fa2f">IFaxRoutingMethod::get_DeviceId</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

