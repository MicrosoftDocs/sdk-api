---
UID: NF:faxcomex.IFaxIncomingJob.get_AvailableOperations
title: IFaxIncomingJob::get_AvailableOperations
author: windows-driver-content
description: Retrieves the AvailableOperations property of a FaxIncomingJob object. The AvailableOperations property indicates the combination of valid operations that you can perform on the fax job given its current status.
old-location: fax\_mfax_faxincomingjob_availableoperations_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0z1v_cpp.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxIncomingJob interface [Fax Service],get_AvailableOperations method, IFaxIncomingJob.get_AvailableOperations, IFaxIncomingJob::get_AvailableOperations, _mfax_faxincomingjob.availableoperations_cpp, fax._mfax_faxincomingjob_availableoperations_cpp, faxcomex/IFaxIncomingJob::get_AvailableOperations, get_AvailableOperations, get_AvailableOperations method [Fax Service], get_AvailableOperations method [Fax Service],IFaxIncomingJob interface
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxIncomingJob.get_AvailableOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingJob::get_AvailableOperations


## -description


Retrieves the <b>AvailableOperations</b> property of a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object. The <b>AvailableOperations</b> property indicates the combination of valid operations that you can perform on the fax job given its current status.


## -parameters




### -param pAvailableOperations






#### - plAvailableOperations [out, retval]

Type: <b><a href="https://msdn.microsoft.com/557655b9-d59b-4255-b071-4c1fbec3a889">FAX_JOB_OPERATIONS_ENUM</a>*</b>

Pointer to a <b>long</b> value from the <a href="https://msdn.microsoft.com/557655b9-d59b-4255-b071-4c1fbec3a889">FAX_JOB_OPERATIONS_ENUM</a> enumeration that specifies a bitwise combination of the operations that you can currently perform on the fax job. Some operations are mutually exclusive. For example, you cannot pause a job that has already been paused. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/04149d5c-e26f-4cef-9ae0-eba2a199ec51">AvailableOperations</a>



<a href="https://msdn.microsoft.com/557655b9-d59b-4255-b071-4c1fbec3a889">FAX_JOB_OPERATIONS_ENUM</a>



<a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>
 

 

