---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagMFASYNCRESULT structure


## -description



          Contains data that is needed to implement the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface.
        


## -struct-fields




### -field overlapped


            An <b>OVERLAPPED</b> structure. This structure is used internally to queue the work item. Fill this member with zeros.
          


### -field pCallback


            Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface. This interface is implemented by the caller of the asynchronous method. This member can be <b>NULL</b>. If this member is <b>NULL</b>, the <b>hEvent</b> member must be a valid event handle.
          


### -field hrStatusResult


            The status code returned when this structure is used with an I/O completion port. You can also use this member to hold the status code for the asynchronous operation, returned by <a href="https://msdn.microsoft.com/ad99f3dd-4885-42e8-8f4e-060d522dde7b">IMFAsyncResult::GetStatus</a>.
          


### -field dwBytesTransferred


            The number of bytes transferred when this structure is used with an I/O completion port. This member is used internally by the work queue. Set this member to zero.
          


### -field hEvent


            Event handle. If <b>pCallback</b> is <b>NULL</b>, set this member to a valid event handle. The event is signaled when the work item is dispatched. Otherwise, set this member to <b>NULL</b>.
          


### -field IMFAsyncResult

 




## -remarks




        Any custom implementation of the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface must inherit this structure. For more information, see <a href="https://msdn.microsoft.com/78cef367-b007-46d5-bb7f-2b3f7eed9926">Custom Asynchronous Result Objects</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/78cef367-b007-46d5-bb7f-2b3f7eed9926">Custom Asynchronous Result Objects</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

