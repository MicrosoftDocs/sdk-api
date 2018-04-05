---
UID: NC:winbio.PWINBIO_ASYNC_COMPLETION_CALLBACK
title: PWINBIO_ASYNC_COMPLETION_CALLBACK
author: windows-driver-content
description: Notifies the client application that an asynchronous operation started by using WinBioAsyncOpenSession or WinBioAsyncOpenFramework has completed.
old-location: secbiomet\pwinbio_async_completion_callback.htm
old-project: SecBioMet
ms.assetid: 550EA13D-18CE-4B73-9C9B-4D5C46C48A75
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PWINBIO_ASYNC_COMPLETION_CALLBACK, PWINBIO_ASYNC_COMPLETION_CALLBACK function pointer [Windows Biometric Framework API], secbiomet.pwinbio_async_completion_callback, winbio/PWINBIO_ASYNC_COMPLETION_CALLBACK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: winbio.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WIN32_STREAM_ID, *LPWIN32_STREAM_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winbio.h
api_name:
-	PWINBIO_ASYNC_COMPLETION_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PWINBIO_ASYNC_COMPLETION_CALLBACK callback


## -description


Called by the Windows Biometric Framework to notify the client application that an asynchronous operation has completed. The callback is defined by the client application and called by the Windows Biometric Framework.


## -parameters




### -param AsyncResult [in]

Pointer to a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure that contains information about the completed operation. The structure is created by the Windows Biometric Framework. You must call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> to release the structure.


## -returns



Do not return a value from your implementation of this function.




## -remarks



You must create this callback if you open a biometric session by using the <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a> function or the <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a> function and you set  <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b> in the <i>NotificationMethod</i> parameter of either function.

<div class="alert"><b>Important</b>  The <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure is allocated internally by the Windows Biometric Framework. Therefore, when you are through using it, call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> to release the allocated memory and avoid leaks. Because this also releases all nested data structures, you should not keep a copy of any pointers returned in the <b>WINBIO_ASYNC_RESULT</b> structure. If you want to save any data returned in a nested structure, make a private copy of that data before calling <b>WinBioFree</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a>



<a href="https://msdn.microsoft.com/e9a0bb5f-4bbd-4dc4-9cd8-c26f5e4f74cf">WinBioOpenSession</a>
 

 

