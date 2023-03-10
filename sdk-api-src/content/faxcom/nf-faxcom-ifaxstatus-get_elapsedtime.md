---
UID: NF:faxcom.IFaxStatus.get_ElapsedTime
title: IFaxStatus::get_ElapsedTime (faxcom.h)
description: Retrieves the ElapsedTime property for the FaxStatus object of a parent FaxPort object. The ElapsedTime property is a number that represents the elapsed time for an active fax job.
helpviewer_keywords: ["ElapsedTime property [Fax Service]","ElapsedTime property [Fax Service]","IFaxStatus interface","IFaxStatus interface [Fax Service]","ElapsedTime property","IFaxStatus.ElapsedTime","IFaxStatus.get_ElapsedTime","IFaxStatus::ElapsedTime","IFaxStatus::get_ElapsedTime","_mfax_ifaxstatus_get_elapsedtime","fax._mfax_ifaxstatus_get_elapsedtime","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_elapsedtime_cpp","faxcom/IFaxStatus::ElapsedTime","faxcom/IFaxStatus::get_ElapsedTime","get_ElapsedTime"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_elapsedtime_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2en9.htm
ms.date: 12/05/2018
ms.keywords: ElapsedTime property [Fax Service], ElapsedTime property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],ElapsedTime property, IFaxStatus.ElapsedTime, IFaxStatus.get_ElapsedTime, IFaxStatus::ElapsedTime, IFaxStatus::get_ElapsedTime, _mfax_ifaxstatus_get_elapsedtime, fax._mfax_ifaxstatus_get_elapsedtime, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_elapsedtime_cpp, faxcom/IFaxStatus::ElapsedTime, faxcom/IFaxStatus::get_ElapsedTime, get_ElapsedTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxStatus::get_ElapsedTime
 - faxcom/IFaxStatus::get_ElapsedTime
dev_langs:
 - c++
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
---

# IFaxStatus::get_ElapsedTime


## -description

Retrieves the <b>ElapsedTime</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>ElapsedTime</b> property is a number that represents the elapsed time for an active fax job.

This property is read-only.

## -parameters

## -remarks

The value of this property is provided in <b>DATE</b> format, but represents elapsed time, not the date and time. The value of this property is undefined if there is no job being executed on the device.

You can use the <b>ElapsedTime</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object in conjunction with the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-starttime-vb">StartTime</a> property of the object to inform users about the transmission length of a fax job.