---
UID: NF:faxcom.IFaxStatus.get_Csid
title: IFaxStatus::get_Csid
author: windows-sdk-content
description: Retrieves the Csid property for the FaxStatus object of a parent FaxPort object. The Csid property is a string that contains called station identifier (CSID) information, typically the fax number of the receiving device.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_csid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6k2s.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Csid property [Fax Service], Csid property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],Csid property, IFaxStatus.Csid, IFaxStatus.get_Csid, IFaxStatus::Csid, IFaxStatus::get_Csid, _mfax_ifaxstatus_get_csid, fax._mfax_ifaxstatus_get_csid, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_csid_cpp, faxcom/IFaxStatus::Csid, faxcom/IFaxStatus::get_Csid, get_Csid
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
 - IFaxStatus.Csid
 - IFaxStatus.get_Csid
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
- IFaxStatus.get_Csid
: 
---

# IFaxStatus::get_Csid


## -description


Retrieves the <b>Csid</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>Csid</b> property is a string that contains called station identifier (CSID) information, typically the fax number of the receiving device.

This property is read-only.


## -parameters


## -remarks



If the CSID information is not available, the <b>IFaxStatus::get_Csid</b> method returns an empty string.

The <b>IFaxStatus::get_Csid</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

