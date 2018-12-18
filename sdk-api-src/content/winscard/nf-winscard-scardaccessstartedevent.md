---
UID: NF:winscard.SCardAccessStartedEvent
title: SCardAccessStartedEvent function
author: windows-sdk-content
description: Returns an event handle when an event signals that the smart card resource manager is started.
old-location: security\scardaccessstartedevent.htm
tech.root: secauthn
ms.assetid: ddfab09d-5477-4c4e-883c-d3c19258c49d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SCardAccessStartedEvent, SCardAccessStartedEvent function [Security], _smart_scardaccessstartedevent, security.scardaccessstartedevent, winscard/SCardAccessStartedEvent
ms.topic: function
req.header: winscard.h
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
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardAccessStartedEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardAccessStartedEvent function


## -description


The <b>SCardAccessStartedEvent</b> function returns an event handle when an event signals that the smart card resource manager is started. The event-object handle can be specified in a call to one of the wait functions.


## -parameters






## -returns



The function returns an event HANDLE if it succeeds or <b>NULL</b> if it fails.

 If the function fails, the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function provides information on the cause of the failure. 




## -remarks



The event-object handle returned can be specified in a call to one of the wait functions.

Do not close the handle returned by this function.
When you have finished using the handle, decrement the reference count by calling the <a href="https://msdn.microsoft.com/2c08500f-3ebf-4267-8436-b67543e1c13c">SCardReleaseStartedEvent</a> function.



