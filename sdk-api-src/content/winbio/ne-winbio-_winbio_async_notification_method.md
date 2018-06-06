---
UID: NE:winbio._WINBIO_ASYNC_NOTIFICATION_METHOD
title: "_WINBIO_ASYNC_NOTIFICATION_METHOD"
author: windows-sdk-content
description: Defines constants that specify how completion notifications for asynchronous operations are to be delivered to the client application.
old-location: secbiomet\winbio_async_notification_method.htm
old-project: SecBioMet
ms.assetid: 3256B178-DF12-4448-B775-CE419F793597
ms.author: windowssdkdev
ms.date: 04/24/2018
ms.keywords: "*PWINBIO_ASYNC_NOTIFICATION_METHOD, WINBIO_ASYNC_NOTIFICATION_METHOD, WINBIO_ASYNC_NOTIFICATION_METHOD enumeration [Windows Biometric Framework API], WINBIO_ASYNC_NOTIFY_CALLBACK, WINBIO_ASYNC_NOTIFY_MAXIMUM_VALUE, WINBIO_ASYNC_NOTIFY_MESSAGE, WINBIO_ASYNC_NOTIFY_NONE, _WINBIO_ASYNC_NOTIFICATION_METHOD, secbiomet.winbio_async_notification_method, winbio/WINBIO_ASYNC_NOTIFICATION_METHOD, winbio/WINBIO_ASYNC_NOTIFY_CALLBACK, winbio/WINBIO_ASYNC_NOTIFY_MAXIMUM_VALUE, winbio/WINBIO_ASYNC_NOTIFY_MESSAGE, winbio/WINBIO_ASYNC_NOTIFY_NONE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WINBIO_ASYNC_NOTIFICATION_METHOD, *PWINBIO_ASYNC_NOTIFICATION_METHOD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio.h
api_name:
 - WINBIO_ASYNC_NOTIFICATION_METHOD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_ASYNC_NOTIFICATION_METHOD enumeration


## -description


Defines constants that specify how completion notifications for asynchronous operations are to be delivered to the client application. This enumeration is used by the <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a> and <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a> functions.


## -enum-fields




### -field WINBIO_ASYNC_NOTIFY_NONE

The operation is synchronous.


### -field WINBIO_ASYNC_NOTIFY_CALLBACK

The client-implemented <a href="https://msdn.microsoft.com/550EA13D-18CE-4B73-9C9B-4D5C46C48A75">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function is called by the framework.


### -field WINBIO_ASYNC_NOTIFY_MESSAGE

The framework sends completion notices to the client application window message queue.


### -field WINBIO_ASYNC_NOTIFY_MAXIMUM_VALUE

The maximum enumeration value. This constant is not directly used by the <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a> and <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a>.


## -remarks



This enumeration was introduced in Windows 8.




## -see-also




<a href="https://msdn.microsoft.com/fd33bc63-cc99-40de-a43b-b0bc7d4c9454">Client Application Enumerations</a>



<a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a>



<a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a>
 

 

