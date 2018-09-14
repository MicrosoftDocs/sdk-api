---
UID: NF:faxcom.IFaxStatus.get_Address
title: IFaxStatus::get_Address
author: windows-sdk-content
description: Retrieves the Address property for the FaxStatus object of a parent FaxPort object. The Address property is a null-terminated string that contains the destination of a fax job.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_address_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_76er.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Address property [Fax Service], Address property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],Address property, IFaxStatus.Address, IFaxStatus.get_Address, IFaxStatus::Address, IFaxStatus::get_Address, _mfax_ifaxstatus_get_address, fax._mfax_ifaxstatus_get_address, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_address_cpp, faxcom/IFaxStatus::Address, faxcom/IFaxStatus::get_Address, get_Address
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
 - IFaxStatus.Address
 - IFaxStatus.get_Address
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_Address


## -description


Retrieves the <b>Address</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>Address</b> property is a null-terminated string that contains the destination of a fax job.

This property is read-only.


## -parameters


## -remarks



The <b>IFaxStatus::get_Address</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

