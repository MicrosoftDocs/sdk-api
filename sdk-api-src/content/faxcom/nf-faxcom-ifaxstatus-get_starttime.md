---
UID: NF:faxcom.IFaxStatus.get_StartTime
title: IFaxStatus::get_StartTime
author: windows-sdk-content
description: Retrieves the StartTime property for the FaxStatus object of a parent FaxPort object. The StartTime property is a number that represents the starting time for an active fax job.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_starttime_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7cmd.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxStatus interface [Fax Service],StartTime property, IFaxStatus.StartTime, IFaxStatus.get_StartTime, IFaxStatus::StartTime, IFaxStatus::get_StartTime, StartTime property [Fax Service], StartTime property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_starttime, fax._mfax_ifaxstatus_get_starttime, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_starttime_cpp, faxcom/IFaxStatus::StartTime, faxcom/IFaxStatus::get_StartTime, get_StartTime
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
 - IFaxStatus.StartTime
 - IFaxStatus.get_StartTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_StartTime


## -description


Retrieves the <b>StartTime</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>StartTime</b> property is a number that represents the starting time for an active fax job.

This property is read-only.


## -parameters


## -remarks



You can use the <b>StartTime</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object in conjunction with the <a href="https://msdn.microsoft.com/b9784976-9844-4937-86e5-979aec8ade72">ElapsedTime</a> property of the object to inform users about the transmission length of a fax job.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/b9784976-9844-4937-86e5-979aec8ade72">IFaxStatus::get_ElapsedTime</a>
 

 

