---
UID: NF:faxcom.IFaxStatus.get_SubmittedTime
title: IFaxStatus::get_SubmittedTime
author: windows-sdk-content
description: Retrieves the SubmittedTime property for the FaxStatus object of a parent FaxPort object. The SubmittedTime property is a number that represents the time the user submitted the active fax job.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_submittedtime_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_46n9.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxStatus interface [Fax Service],SubmittedTime property, IFaxStatus.SubmittedTime, IFaxStatus.get_SubmittedTime, IFaxStatus::SubmittedTime, IFaxStatus::get_SubmittedTime, SubmittedTime property [Fax Service], SubmittedTime property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_submittedtime, fax._mfax_ifaxstatus_get_submittedtime, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_submittedtime_cpp, faxcom/IFaxStatus::SubmittedTime, faxcom/IFaxStatus::get_SubmittedTime, get_SubmittedTime
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
 - IFaxStatus.SubmittedTime
 - IFaxStatus.get_SubmittedTime
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
- IFaxStatus.get_SubmittedTime
: 
---

# IFaxStatus::get_SubmittedTime


## -description


Retrieves the <b>SubmittedTime</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>SubmittedTime</b> property is a number that represents the time the user submitted the active fax job.

This property is read-only.


## -parameters


## -remarks



You can use the <b>SubmittedTime</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object in conjunction with the <a href="https://msdn.microsoft.com/2093664f-de48-4f8e-a047-4696377c6fd6">StartTime</a> property of the object to provide users with information about a fax job.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/239b98c5-be46-4e54-83f7-eb7f6250fa57">IFaxStatus::get_Send</a>



<a href="https://msdn.microsoft.com/2093664f-de48-4f8e-a047-4696377c6fd6">IFaxStatus::get_StartTime</a>
 

 

