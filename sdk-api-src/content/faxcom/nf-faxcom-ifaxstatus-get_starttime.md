---
UID: NF:faxcom.IFaxStatus.get_StartTime
title: IFaxStatus::get_StartTime
author: windows-sdk-content
description: Retrieves the StartTime property for the FaxStatus object of a parent FaxPort object. The StartTime property is a number that represents the starting time for an active fax job.
old-location: fax\_mfax_ifaxstatus_get_starttime_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7cmd.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxStatus object [Fax Service],StartTime property, FaxStatus.StartTime, IFaxStatus.get_StartTime, IFaxStatus::get_StartTime, StartTime property [Fax Service], StartTime property [Fax Service],FaxStatus object, _mfax_ifaxstatus_get_starttime, fax._mfax_ifaxstatus_get_starttime, fax._mfax_ifaxstatus_get_starttime_vb, get_StartTime
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - FaxStatus.StartTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxStatus::get_StartTime


## -description


Retrieves the <b>StartTime</b> property for the <a href="https://msdn.microsoft.com/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>StartTime</b> property is a number that represents the starting time for an active fax job.

This property is read-only.


## -parameters


## -remarks



You can use the <b>StartTime</b> property of a <a href="https://msdn.microsoft.com/library/ms691355(v=VS.85).aspx">FaxStatus</a> object in conjunction with the <a href="https://msdn.microsoft.com/en-us/library/ms691311(v=VS.85).aspx">ElapsedTime</a> property of the object to inform users about the transmission length of a fax job.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691311(v=VS.85).aspx">ElapsedTime</a>



<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690310(v=VS.85).aspx">FaxStatus</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/library/ms690794(v=VS.85).aspx">IFaxStatus</a>
 

 

