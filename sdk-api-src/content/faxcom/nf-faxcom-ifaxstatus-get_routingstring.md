---
UID: NF:faxcom.IFaxStatus.get_RoutingString
title: IFaxStatus::get_RoutingString
author: windows-sdk-content
description: Retrieves the RoutingString property for the FaxStatus object of a parent FaxPort object. The RoutingString property is a null-terminated string that contains routing information for inbound fax transmissions that is specific to a fax service provider.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_routingstring_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1aav.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxStatus interface [Fax Service],RoutingString property, IFaxStatus.RoutingString, IFaxStatus.get_RoutingString, IFaxStatus::RoutingString, IFaxStatus::get_RoutingString, RoutingString property [Fax Service], RoutingString property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_routingstring, fax._mfax_ifaxstatus_get_routingstring, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_routingstring_cpp, faxcom/IFaxStatus::RoutingString, faxcom/IFaxStatus::get_RoutingString, get_RoutingString
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
 - IFaxStatus.RoutingString
 - IFaxStatus.get_RoutingString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_RoutingString


## -description


Retrieves the <b>RoutingString</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>RoutingString</b> property is a null-terminated string that contains routing information for inbound fax transmissions that is specific to a fax service provider.

This property is read-only.


## -parameters


## -remarks



The <b>IFaxStatus::get_RoutingString</b> method sets the <i>pVal</i> parameter to optional inbound routing information, if it is available. If the information is not available, the method returns an empty string.

The <b>IFaxStatus::get_RoutingString</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/e7a63893-d8df-4253-80b0-3faab13934fd">IFaxStatus::get_Receive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

