---
UID: NF:faxcom.IFaxStatus.get_SubmittedTime
title: IFaxStatus::get_SubmittedTime (faxcom.h)
description: Retrieves the SubmittedTime property for the FaxStatus object of a parent FaxPort object. The SubmittedTime property is a number that represents the time the user submitted the active fax job.
helpviewer_keywords: ["IFaxStatus interface [Fax Service]","SubmittedTime property","IFaxStatus.SubmittedTime","IFaxStatus.get_SubmittedTime","IFaxStatus::SubmittedTime","IFaxStatus::get_SubmittedTime","SubmittedTime property [Fax Service]","SubmittedTime property [Fax Service]","IFaxStatus interface","_mfax_ifaxstatus_get_submittedtime","fax._mfax_ifaxstatus_get_submittedtime","fax._mfax_ifaxstatus_mfax_ifaxstatus_get_submittedtime_cpp","faxcom/IFaxStatus::SubmittedTime","faxcom/IFaxStatus::get_SubmittedTime","get_SubmittedTime"]
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_submittedtime_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_46n9.htm
ms.date: 12/05/2018
ms.keywords: IFaxStatus interface [Fax Service],SubmittedTime property, IFaxStatus.SubmittedTime, IFaxStatus.get_SubmittedTime, IFaxStatus::SubmittedTime, IFaxStatus::get_SubmittedTime, SubmittedTime property [Fax Service], SubmittedTime property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_submittedtime, fax._mfax_ifaxstatus_get_submittedtime, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_submittedtime_cpp, faxcom/IFaxStatus::SubmittedTime, faxcom/IFaxStatus::get_SubmittedTime, get_SubmittedTime
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
 - IFaxStatus::get_SubmittedTime
 - faxcom/IFaxStatus::get_SubmittedTime
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
 - IFaxStatus.SubmittedTime
 - IFaxStatus.get_SubmittedTime
---

# IFaxStatus::get_SubmittedTime


## -description

Retrieves the <b>SubmittedTime</b> property for the <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>SubmittedTime</b> property is a number that represents the time the user submitted the active fax job.

This property is read-only.

## -parameters

## -remarks

You can use the <b>SubmittedTime</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object in conjunction with the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-starttime-vb">StartTime</a> property of the object to provide users with information about a fax job.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxstatus">IFaxStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-send-vb">IFaxStatus::get_Send</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-starttime-vb">IFaxStatus::get_StartTime</a>