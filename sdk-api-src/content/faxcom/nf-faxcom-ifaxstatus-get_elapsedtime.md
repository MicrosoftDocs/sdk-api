---
UID: NF:faxcom.IFaxStatus.get_ElapsedTime
title: IFaxStatus::get_ElapsedTime method
author: windows-driver-content
description: Retrieves the ElapsedTime property for the FaxStatus object of a parent FaxPort object. The ElapsedTime property is a number that represents the elapsed time for an active fax job.
old-location: fax\_mfax_ifaxstatus_get_elapsedtime_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2en9.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: ElapsedTime property [Fax Service], ElapsedTime property [Fax Service], FaxStatus object, FaxStatus object [Fax Service], ElapsedTime property, IFaxStatus, IFaxStatus::get_ElapsedTime, _mfax_ifaxstatus_get_elapsedtime, fax._mfax_ifaxstatus_get_elapsedtime, fax._mfax_ifaxstatus_get_elapsedtime_vb, get_ElapsedTime,IFaxStatus.get_ElapsedTime
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	FaxStatus.ElapsedTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxStatus::get_ElapsedTime method


## -description


Retrieves the <b>ElapsedTime</b> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>ElapsedTime</b> property is a number that represents the elapsed time for an active fax job.

This property is read-only.


## -parameters


## -remarks



The value of this property is provided in <b>Date</b> format, but represents elapsed time, not the date and time. The value of this property is undefined if there is no job being executed on the device.

You can use the <b>ElapsedTime</b> property of a <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object in conjunction with the <a href="https://msdn.microsoft.com/c9611619-b7b4-486d-b8fa-a8de8a50fae4">StartTime</a> property of the object to inform users about the transmission length of a fax job.



