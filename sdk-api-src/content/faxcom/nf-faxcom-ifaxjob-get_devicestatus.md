---
UID: NF:faxcom.IFaxJob.get_DeviceStatus
title: IFaxJob::get_DeviceStatus
author: windows-sdk-content
description: The IFaxJob::get_DeviceStatus property is a null-terminated string that describes the status of the port associated with the fax job.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_devicestatus_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1dwz.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Aborting, Answered, Available, Bad Address, Busy, Call Blacklisted, Call Delayed, Completed, DeviceStatus property [Fax Service], DeviceStatus property [Fax Service],IFaxJob interface, Dialing, Disconnected, Fatal Error, Handled, IFaxJob interface [Fax Service],DeviceStatus property, IFaxJob.DeviceStatus, IFaxJob.get_DeviceStatus, IFaxJob::DeviceStatus, IFaxJob::get_DeviceStatus, Initializing, No Answer, No Dial Tone, Not a Fax Call, Offline, Receiving, Ringing, Routing, Sending, Unavailable, _mfax_ifaxjob_get_devicestatus, fax._mfax_ifaxjob_get_devicestatus, fax._mfax_ifaxjob_mfax_ifaxjob_get_devicestatus_cpp, faxcom/IFaxJob::DeviceStatus, faxcom/IFaxJob::get_DeviceStatus, get_DeviceStatus
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
 - IFaxJob.DeviceStatus
 - IFaxJob.get_DeviceStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJob::get_DeviceStatus


## -description


The <b>IFaxJob::get_DeviceStatus</b> property is a null-terminated string that describes the status of the port associated with the fax job.

This property is read-only.


## -parameters


## -remarks



If the job is in the job queue waiting transmission, the fax server has not associated a device with the job. In this instance, <b>IFaxJob::get_DeviceStatus</b> is "Unknown". 

<b>IFaxJob::get_DeviceStatus</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>
 

 

