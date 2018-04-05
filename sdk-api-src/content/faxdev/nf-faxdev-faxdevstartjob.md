---
UID: NF:faxdev.FaxDevStartJob
title: FaxDevStartJob function
author: windows-driver-content
description: The fax service calls the FaxDevStartJob function to initialize a new fax job. The fax service also calls FaxDevStartJob to signal the beginning of each fax operation to the fax service provider (FSP). Each FSP must export the FaxDevStartJob function.
old-location: fax\_mfax_faxdevstartjob.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_5ode.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: FaxDevStartJob, FaxDevStartJob function [Fax Service], _mfax_faxdevstartjob, fax._mfax_faxdevstartjob, faxdev/FaxDevStartJob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: faxdev.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
-	UserDefined
api_location:
-	FaxDev.h
api_name:
-	FaxDevStartJob
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FaxDevStartJob function


## -description


The fax service calls the <b>FaxDevStartJob</b> function to initialize a new fax job. The fax service also calls <b>FaxDevStartJob</b> to signal the beginning of each fax operation to the fax service provider (FSP). Each FSP must export the <b>FaxDevStartJob</b> function.


## -parameters




### -param LineHandle [in]

Type: <b>HLINE</b>

Specifies a handle to the open line device associated with the fax job.


### -param DeviceId [in]

Type: <b>DWORD</b>

Specifies the TAPI line device identifier associated with the fax job.


### -param FaxHandle [out]

Type: <b>PHANDLE</b>

Pointer to a variable that receives a fax handle associated with the fax job. The FSP must set this handle to a meaningful value; this handle usually specifies a pointer to a block of memory with job-specific instance data.


### -param CompletionPortHandle [in]

Type: <b>HANDLE</b>

Specifies a handle to an I/O completion port. For more information, see <a href="https://msdn.microsoft.com/213c48e8-bb21-43ed-9c00-2a5cf8ac25f0">I/O Completion Ports</a>.


### -param CompletionKey [in]

Type: <b>ULONG_PTR</b>

Specifies a completion key value. The fax service provider should pass this opaque value to the <a href="https://msdn.microsoft.com/69a9b1e5-2d40-42de-a14a-f7b6f29bf571">PostQueuedCompletionStatus</a> function.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>FaxDevStartJob</b> function provides an opportunity for the fax service provider to perform call setup.

The fax service calls <b>FaxDevStartJob</b> at the beginning of a new fax job and once for each fax operation. This is because each operation executes in a separate thread. It calls <b>FaxDevStartJob</b> just before the <a href="https://msdn.microsoft.com/9ec25812-658f-4d64-85c4-8ab66be5d93e">FaxDevSend</a> function call for a fax send operation, and just before the <a href="https://msdn.microsoft.com/3f37c113-2971-4092-8753-b0d30b8ce6c1">FaxDevReceive</a> function call for a fax receive operation. For more information, see <a href="https://msdn.microsoft.com/af0e3837-5fcb-43da-a951-70b70a9722b1">Operating in a Multithreaded Environment</a>.

The FSP should create an I/O completion packet and call the <a href="https://msdn.microsoft.com/69a9b1e5-2d40-42de-a14a-f7b6f29bf571">PostQueuedCompletionStatus</a> function when the FSP changes its status. One example of a status change is when the FSP finishes receiving or sending fax transmission pages. The completion packet must be a <a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">FAX_DEV_STATUS</a> structure. The FSP must allocate memory for the structure from the heap indicated by the <i>HeapHandle</i> parameter passed to the <a href="https://msdn.microsoft.com/74c4ebad-c1a5-48a4-9ced-548ab21b3c3c">FaxDevInitialize</a> function. The fax service provider must pass the size of the memory allocated to the <i>dwNumberOfBytesTransferred</i> parameter of the PostQueuedCompletionStatus method. The fax service frees any memory allocated for the completion packet structure.

The FSP should use the <i>CompletionPortHandle</i> and <i>CompletionKey</i> parameters to post completion packets for FSP status changes. This method of status notification optimizes performance because the fax service does not need to poll FSPs to obtain updated status information. For more information, see <a href="https://msdn.microsoft.com/d9a99db4-d8f1-4951-8f12-da743c03487f">Creating a Completion Packet</a>.




## -see-also




<a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">FAX_DEV_STATUS</a>



<a href="https://msdn.microsoft.com/402583fd-aef8-4197-a41e-870825c58351">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/f5a0c728-1a3f-46aa-8de8-f47a18425e1a">FaxDevEndJob</a>



<a href="https://msdn.microsoft.com/74c4ebad-c1a5-48a4-9ced-548ab21b3c3c">FaxDevInitialize</a>



<a href="https://msdn.microsoft.com/3f37c113-2971-4092-8753-b0d30b8ce6c1">FaxDevReceive</a>



<a href="https://msdn.microsoft.com/9ec25812-658f-4d64-85c4-8ab66be5d93e">FaxDevSend</a>



<a href="https://msdn.microsoft.com/69a9b1e5-2d40-42de-a14a-f7b6f29bf571">PostQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/a8788e8a-e97c-4082-8e89-b6f4a7568d3a">Using the Fax Service Provider API</a>
 

 

