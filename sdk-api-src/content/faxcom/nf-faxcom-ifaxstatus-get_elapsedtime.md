---
UID: NF:faxcom.IFaxStatus.get_ElapsedTime
title: IFaxStatus::get_ElapsedTime
author: windows-sdk-content
description: Retrieves the ElapsedTime property for the FaxStatus object of a parent FaxPort object. The ElapsedTime property is a number that represents the elapsed time for an active fax job.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_elapsedtime_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2en9.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ElapsedTime property [Fax Service], ElapsedTime property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],ElapsedTime property, IFaxStatus.ElapsedTime, IFaxStatus.get_ElapsedTime, IFaxStatus::ElapsedTime, IFaxStatus::get_ElapsedTime, _mfax_ifaxstatus_get_elapsedtime, fax._mfax_ifaxstatus_get_elapsedtime, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_elapsedtime_cpp, faxcom/IFaxStatus::ElapsedTime, faxcom/IFaxStatus::get_ElapsedTime, get_ElapsedTime
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
 - IFaxStatus.ElapsedTime
 - IFaxStatus.get_ElapsedTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_ElapsedTime


## -description


Retrieves the <b>ElapsedTime</b> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>ElapsedTime</b> property is a number that represents the elapsed time for an active fax job.

This property is read-only.


## -parameters


## -remarks



The value of this property is provided in <b>DATE</b> format, but represents elapsed time, not the date and time. The value of this property is undefined if there is no job being executed on the device.

You can use the <b>ElapsedTime</b> property of a <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object in conjunction with the <a href="https://msdn.microsoft.com/2093664f-de48-4f8e-a047-4696377c6fd6">StartTime</a> property of the object to inform users about the transmission length of a fax job.



