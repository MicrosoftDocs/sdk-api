---
UID: NF:faxcom.IFaxStatus.get_StartTime
title: IFaxStatus::get_StartTime (faxcom.h)
description: Retrieves the StartTime property for the FaxStatus object of a parent FaxPort object. The StartTime property is a number that represents the starting time for an active fax job.
helpviewer_keywords: ["IFaxStatus interface [Fax Service]","StartTime property","IFaxStatus.StartTime","IFaxStatus.get_StartTime","IFaxStatus::StartTime","IFaxStatus::get_StartTime","StartTime property [Fax Service]","StartTime property [Fax Service]","IFaxStatus interface","_mfax_ifaxstatus_get_starttime","fax._mfax_ifaxstatus_get_starttime","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_starttime_cpp","faxcom/IFaxStatus::StartTime","faxcom/IFaxStatus::get_StartTime","get_StartTime"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_starttime_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7cmd.htm
ms.date: 12/05/2018
ms.keywords: IFaxStatus interface [Fax Service],StartTime property, IFaxStatus.StartTime, IFaxStatus.get_StartTime, IFaxStatus::StartTime, IFaxStatus::get_StartTime, StartTime property [Fax Service], StartTime property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_starttime, fax._mfax_ifaxstatus_get_starttime, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_starttime_cpp, faxcom/IFaxStatus::StartTime, faxcom/IFaxStatus::get_StartTime, get_StartTime
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
 - IFaxStatus::get_StartTime
 - faxcom/IFaxStatus::get_StartTime
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
 - IFaxStatus.StartTime
 - IFaxStatus.get_StartTime
---

# IFaxStatus::get_StartTime


## -description

Retrieves the <b>StartTime</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>StartTime</b> property is a number that represents the starting time for an active fax job.

This property is read-only.

## -parameters

## -remarks

You can use the <b>StartTime</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object in conjunction with the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-elapsedtime-vb">ElapsedTime</a> property of the object to inform users about the transmission length of a fax job.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-elapsedtime-vb">IFaxStatus::get_ElapsedTime</a>