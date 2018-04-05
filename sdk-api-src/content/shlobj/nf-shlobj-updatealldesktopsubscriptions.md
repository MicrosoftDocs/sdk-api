---
UID: NF:shlobj.UpdateAllDesktopSubscriptions
title: UpdateAllDesktopSubscriptions function
author: windows-driver-content
description: Deprecated. Enumerates the URLs of all the Desktop components and then tests to see if they are subscribed to. If they are subscribed to, the subscriptions are delivered.
old-location: shell\UpdateAllDesktopSubscriptions.htm
old-project: shell
ms.assetid: 731bac41-ca1f-4bee-9314-28b5773eb694
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: UpdateAllDesktopSubscriptions, UpdateAllDesktopSubscriptions function [Windows Shell], _win32_UpdateAllDesktopSubscriptions, shell.UpdateAllDesktopSubscriptions, shlobj/UpdateAllDesktopSubscriptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	UpdateAllDesktopSubscriptions
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# UpdateAllDesktopSubscriptions function


## -description


Deprecated. Enumerates the URLs of all the Desktop components and then tests to see if they are subscribed to. If they are subscribed to, the subscriptions are delivered.


## -parameters






#### - padp2

Type: <b><a href="https://msdn.microsoft.com/f67cc6c0-183c-4da2-9648-68a86dccfd78">IADesktopP2</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/f67cc6c0-183c-4da2-9648-68a86dccfd78">IADesktopP2</a> interface.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if components are subscribed to; otherwise <b>FALSE</b>.



