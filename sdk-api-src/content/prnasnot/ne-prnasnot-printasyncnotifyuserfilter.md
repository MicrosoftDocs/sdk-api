---
UID: NE:prnasnot.PrintAsyncNotifyUserFilter
title: PrintAsyncNotifyUserFilter
author: windows-sdk-content
description: Specifies whether notifications will go only to listening applications that are associated with the same user as the Print Spooler-hosted sender, or go to a broader set of listening applications.
old-location: gdi\printasyncnotifyuserfilter.htm
tech.root: printdocs
ms.assetid: 89893e25-486a-4cef-b1a6-f812c8cc1fe2
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: PrintAsyncNotifyUserFilter, PrintAsyncNotifyUserFilter enumeration [Windows GDI], _win32_PrintAsyncNotifyUserFilter, gdi.printasyncnotifyuserfilter, kAllUsers, kPerUser, prnasnot/PrintAsyncNotifyUserFilter, prnasnot/kAllUsers, prnasnot/kPerUser
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: prnasnot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - prnasnot.h
api_name:
 - PrintAsyncNotifyUserFilter
product: Windows
targetos: Windows
req.typenames: PrintAsyncNotifyUserFilter
req.redist: 
---

# PrintAsyncNotifyUserFilter enumeration


## -description


Specifies whether notifications will go only to listening applications that are associated with the same user as the Print Spooler-hosted sender, or go to a broader set of listening applications.


## -enum-fields




### -field kPerUser

When passed to <a href="https://msdn.microsoft.com/52cc586a-a565-46c6-b1b7-8613ad111ed3">CreatePrintAsyncNotifyChannel
</a>, kPerUser indicates that notifications will go only to listening applications that are using <a href="https://msdn.microsoft.com/a3f74372-bdc9-43eb-b72f-7d00a43e78a8">Client Impersonation</a> to impersonate the same user as the Print Spooler-hosted sender. For example, if the Print Spooler-hosted sender sends a notification that a print job has finished printing, only listening applications impersonating the user that submitted the job will receive notification. When passed to <a href="https://msdn.microsoft.com/f5a01819-75d0-42a0-b66f-5a25a48b091c">RegisterForPrintAsyncNotifications</a>, kPerUser indicates that the listener will receive notifications only from senders that are impersonating the same user as the listener.


### -field kAllUsers

When passed to <a href="https://msdn.microsoft.com/52cc586a-a565-46c6-b1b7-8613ad111ed3">CreatePrintAsyncNotifyChannel
</a>, kAllUsers indicates that notifications will go to all listening applications, regardless of the user; as long as the sender has administration privileges on the associated print queue or print server. When passed to <a href="https://msdn.microsoft.com/f5a01819-75d0-42a0-b66f-5a25a48b091c">RegisterForPrintAsyncNotifications</a>, kAllUsers indicates that notifications will go to all listening applications whose associated user has administration privileges on the print queue or print server.


## -remarks



Regardless of which value is passed, listeners will receive only the types of notifications for which they have registered.

A user may be simultaneously logged on to multiple terminal server sessions. All of the user's applications, regardless of which session hosts them, will receive notifications for which they have registered.



