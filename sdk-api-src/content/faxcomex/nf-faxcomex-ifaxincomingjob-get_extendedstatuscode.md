---
UID: NF:faxcomex.IFaxIncomingJob.get_ExtendedStatusCode
title: IFaxIncomingJob::get_ExtendedStatusCode
author: windows-sdk-content
description: Retrieves the ExtendedStatusCode property of a FaxIncomingJob object. The ExtendedStatusCode property specifies a code describing the job's extended status.
old-location: fax\_mfax_faxincomingjob_extendedstatuscode_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_40v9_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxIncomingJob interface [Fax Service],get_ExtendedStatusCode method, IFaxIncomingJob.get_ExtendedStatusCode, IFaxIncomingJob::get_ExtendedStatusCode, _mfax_faxincomingjob.extendedstatuscode_cpp, fax._mfax_faxincomingjob_extendedstatuscode_cpp, faxcomex/IFaxIncomingJob::get_ExtendedStatusCode, get_ExtendedStatusCode, get_ExtendedStatusCode method [Fax Service], get_ExtendedStatusCode method [Fax Service],IFaxIncomingJob interface
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
 - IFaxIncomingJob.get_ExtendedStatusCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingJob::get_ExtendedStatusCode


## -description


Retrieves the <b>ExtendedStatusCode</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms684876(v=VS.85).aspx">FaxIncomingJob</a> object. The <b>ExtendedStatusCode</b> property specifies a code describing the job's extended status.


## -parameters




### -param pExtendedStatusCode [out, retval]

Type: <b><a href="https://msdn.microsoft.com/f0cb862b-cb5c-40bd-9df9-a32f849e45a1">FAX_JOB_EXTENDED_STATUS_ENUM</a>*</b>

Pointer to a value from the <a href="https://msdn.microsoft.com/f0cb862b-cb5c-40bd-9df9-a32f849e45a1">FAX_JOB_EXTENDED_STATUS_ENUM</a> enumeration that specifies the extended job status.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/15333cd3-e71a-451c-ae93-9e217ea0895c">ExtendedStatusCode</a>



<a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>
 

 

