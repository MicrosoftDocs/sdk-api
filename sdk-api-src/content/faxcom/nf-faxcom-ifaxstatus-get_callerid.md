---
UID: NF:faxcom.IFaxStatus.get_CallerId
title: IFaxStatus::get_CallerId
author: windows-sdk-content
description: Retrieves the CallerId property for the FaxStatus object of a parent FaxPort object. The CallerId property is a string that identifies the calling device that sent an inbound fax job.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_callerid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3kx0.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CallerId property [Fax Service], CallerId property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],CallerId property, IFaxStatus.CallerId, IFaxStatus.get_CallerId, IFaxStatus::CallerId, IFaxStatus::get_CallerId, _mfax_ifaxstatus_get_callerid, fax._mfax_ifaxstatus_get_callerid, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_callerid_cpp, faxcom/IFaxStatus::CallerId, faxcom/IFaxStatus::get_CallerId, get_CallerId
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
 - IFaxStatus.CallerId
 - IFaxStatus.get_CallerId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_CallerId


## -description


Retrieves the <b>CallerId</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>CallerId</b> property is a string that identifies the calling device that sent an inbound fax job.

This property is read-only.


## -parameters


## -remarks



If caller identification information is not available, the <b>IFaxStatus::get_CallerId</b> method returns an empty string.

The <b>IFaxStatus::get_CallerId</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

