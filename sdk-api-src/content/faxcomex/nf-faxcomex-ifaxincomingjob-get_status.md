---
UID: NF:faxcomex.IFaxIncomingJob.get_Status
title: IFaxIncomingJob::get_Status
author: windows-sdk-content
description: Retrieves the Status property of a FaxIncomingJob object. The Status property is a number that indicates the current status of an inbound fax job in the job queue.
old-location: fax\_mfax_faxincomingjob_status_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1far_cpp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxIncomingJob interface [Fax Service],get_Status method, IFaxIncomingJob.get_Status, IFaxIncomingJob::get_Status, _mfax_faxincomingjob.status_cpp, fax._mfax_faxincomingjob_status_cpp, faxcomex/IFaxIncomingJob::get_Status, get_Status, get_Status method [Fax Service], get_Status method [Fax Service],IFaxIncomingJob interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxIncomingJob.get_Status
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingJob::get_Status


## -description


Retrieves the <b>Status</b> property of a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object. The <b>Status</b> property is a number that indicates the current status of an inbound fax job in the job queue.


## -parameters




### -param pStatus [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7629c51e-2108-4fc6-9870-9500a7fffa62">FAX_JOB_STATUS_ENUM</a>*</b>

Pointer to a value from the <a href="https://msdn.microsoft.com/7629c51e-2108-4fc6-9870-9500a7fffa62">FAX_JOB_STATUS_ENUM</a> enumeration that specifies the current status of an inbound fax job in the job queue.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7629c51e-2108-4fc6-9870-9500a7fffa62">FAX_JOB_STATUS_ENUM</a>



<a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>



<a href="https://msdn.microsoft.com/fd84a3b4-a7ce-400c-a8a9-8134d7308bef">Status</a>
 

 

