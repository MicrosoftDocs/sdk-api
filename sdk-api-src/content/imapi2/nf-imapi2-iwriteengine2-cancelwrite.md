---
UID: NF:imapi2.IWriteEngine2.CancelWrite
title: IWriteEngine2::CancelWrite
author: windows-driver-content
description: Cancels a write operation that is in progress.
old-location: imapi\iwriteengine2_cancelwrite.htm
old-project: imapi
ms.assetid: cd658bd3-71ab-4e63-adec-8b7405a76c12
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: CancelWrite, CancelWrite method [IMAPI], CancelWrite method [IMAPI],IWriteEngine2 interface, IWriteEngine2 interface [IMAPI],CancelWrite method, IWriteEngine2.CancelWrite, IWriteEngine2::CancelWrite, imapi.iwriteengine2_cancelwrite, imapi2/IWriteEngine2::CancelWrite
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IWriteEngine2.CancelWrite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWriteEngine2::CancelWrite


## -description


Cancels a write operation that is in progress. 


## -parameters






## -returns



The following values are returned on success, but other success codes may be returned as a result of implementation: The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_IMAPI_WRITE_NOT_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The 'write' operation initiated by the last call to <a href="https://msdn.microsoft.com/a6158984-04d3-4919-8a67-fc860b4b3a47">IWriteEngine2::WriteSection</a> has not yet begun, and cannot be canceled.   It is recommended to call  <a href="https://msdn.microsoft.com/cd658bd3-71ab-4e63-adec-8b7405a76c12">IWriteEngine2::CancelWrite</a>  until a different success code is returned.

Value: 0x00AA0302L

</td>
</tr>
</table>
 

The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
</table>
 




## -remarks



To cancel the write operation, you must call this method from the <a href="https://msdn.microsoft.com/efee838d-aa6e-41a0-aafb-64ba6ca19f29">DWriteEngine2Events::Update</a> event handler that you implemented. 




## -see-also




<a href="https://msdn.microsoft.com/697f8247-6940-4b5e-8521-df89838837be">DWriteEngine2Events</a>



<a href="https://msdn.microsoft.com/89e7526f-2b9b-4f37-b537-5046a0ac283d">IWriteEngine2</a>



<a href="https://msdn.microsoft.com/a6158984-04d3-4919-8a67-fc860b4b3a47">IWriteEngine2::WriteSection</a>



<a href="https://msdn.microsoft.com/88f67eab-c87b-4a15-b29f-25675d0cac22">IWriteEngine2::get_WriteInProgress</a>
 

 

