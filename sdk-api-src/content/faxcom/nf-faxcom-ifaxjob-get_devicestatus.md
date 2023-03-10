---
UID: NF:faxcom.IFaxJob.get_DeviceStatus
title: IFaxJob::get_DeviceStatus (faxcom.h)
description: The IFaxJob::get_DeviceStatus property is a null-terminated string that describes the status of the port associated with the fax job.
helpviewer_keywords: ["Aborting","Answered","Available","Bad Address","Busy","Call Blocklisted","Call Delayed","Completed","DeviceStatus property [Fax Service]","DeviceStatus property [Fax Service]","IFaxJob interface","Dialing","Disconnected","Fatal Error","Handled","IFaxJob interface [Fax Service]","DeviceStatus property","IFaxJob.DeviceStatus","IFaxJob.get_DeviceStatus","IFaxJob::DeviceStatus","IFaxJob::get_DeviceStatus","Initializing","No Answer","No Dial Tone","Not a Fax Call","Offline","Receiving","Ringing","Routing","Sending","Unavailable","_mfax_ifaxjob_get_devicestatus","fax._mfax_ifaxjob_get_devicestatus","fax._mfax_ifaxjob_mfax_ifaxjob_get_devicestatus_cpp","faxcom/IFaxJob::DeviceStatus","faxcom/IFaxJob::get_DeviceStatus","get_DeviceStatus"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_devicestatus_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1dwz.htm
ms.date: 12/05/2018
ms.keywords: Aborting, Answered, Available, Bad Address, Busy, Call Blocklisted, Call Delayed, Completed, DeviceStatus property [Fax Service], DeviceStatus property [Fax Service],IFaxJob interface, Dialing, Disconnected, Fatal Error, Handled, IFaxJob interface [Fax Service],DeviceStatus property, IFaxJob.DeviceStatus, IFaxJob.get_DeviceStatus, IFaxJob::DeviceStatus, IFaxJob::get_DeviceStatus, Initializing, No Answer, No Dial Tone, Not a Fax Call, Offline, Receiving, Ringing, Routing, Sending, Unavailable, _mfax_ifaxjob_get_devicestatus, fax._mfax_ifaxjob_get_devicestatus, fax._mfax_ifaxjob_mfax_ifaxjob_get_devicestatus_cpp, faxcom/IFaxJob::DeviceStatus, faxcom/IFaxJob::get_DeviceStatus, get_DeviceStatus
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
 - IFaxJob::get_DeviceStatus
 - faxcom/IFaxJob::get_DeviceStatus
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
 - IFaxJob.DeviceStatus
 - IFaxJob.get_DeviceStatus
---

# IFaxJob::get_DeviceStatus


## -description

The <b>IFaxJob::get_DeviceStatus</b> property is a null-terminated string that describes the status of the port associated with the fax job.

This property is read-only.

## -parameters

## -remarks

If the job is in the job queue waiting transmission, the fax server has not associated a device with the job. In this instance, <b>IFaxJob::get_DeviceStatus</b> is "Unknown". 

<b>IFaxJob::get_DeviceStatus</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>