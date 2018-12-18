---
UID: NF:faxcom.IFaxStatus.get_Tsid
title: IFaxStatus::get_Tsid
author: windows-sdk-content
description: Retrieves the Tsid property for the FaxStatus object of a parent FaxPort object. The Tsid property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_tsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_22p0.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxStatus interface [Fax Service],Tsid property, IFaxStatus.Tsid, IFaxStatus.get_Tsid, IFaxStatus::Tsid, IFaxStatus::get_Tsid, Tsid property [Fax Service], Tsid property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_tsid, fax._mfax_ifaxstatus_get_tsid, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_tsid_cpp, faxcom/IFaxStatus::Tsid, faxcom/IFaxStatus::get_Tsid, get_Tsid
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
 - IFaxStatus.Tsid
 - IFaxStatus.get_Tsid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_Tsid


## -description


Retrieves the <b>Tsid</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>Tsid</b> property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.

This property is read-only.


## -parameters


## -remarks



The <b>Tsid</b> property is set for both inbound and outbound fax transmissions. If the TSID information is not available, the <b>IFaxStatus::get_Tsid</b> method returns an empty string.

The <b>IFaxStatus::get_Tsid</b> method allocates the memory required for the buffer pointed to by the pVal parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

