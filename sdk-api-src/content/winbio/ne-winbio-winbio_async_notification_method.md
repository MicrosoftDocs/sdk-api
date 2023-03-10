---
UID: NE:winbio._WINBIO_ASYNC_NOTIFICATION_METHOD
title: WINBIO_ASYNC_NOTIFICATION_METHOD (winbio.h)
description: Defines constants that specify how completion notifications for asynchronous operations are to be delivered to the client application.
helpviewer_keywords: ["*PWINBIO_ASYNC_NOTIFICATION_METHOD","WINBIO_ASYNC_NOTIFICATION_METHOD","WINBIO_ASYNC_NOTIFICATION_METHOD enumeration [Windows Biometric Framework API]","WINBIO_ASYNC_NOTIFY_CALLBACK","WINBIO_ASYNC_NOTIFY_MAXIMUM_VALUE","WINBIO_ASYNC_NOTIFY_MESSAGE","WINBIO_ASYNC_NOTIFY_NONE","secbiomet.winbio_async_notification_method","winbio/WINBIO_ASYNC_NOTIFICATION_METHOD","winbio/WINBIO_ASYNC_NOTIFY_CALLBACK","winbio/WINBIO_ASYNC_NOTIFY_MAXIMUM_VALUE","winbio/WINBIO_ASYNC_NOTIFY_MESSAGE","winbio/WINBIO_ASYNC_NOTIFY_NONE"]
old-location: secbiomet\winbio_async_notification_method.htm
tech.root: SecBioMet
ms.assetid: 3256B178-DF12-4448-B775-CE419F793597
ms.date: 12/05/2018
ms.keywords: '*PWINBIO_ASYNC_NOTIFICATION_METHOD, WINBIO_ASYNC_NOTIFICATION_METHOD, WINBIO_ASYNC_NOTIFICATION_METHOD enumeration [Windows Biometric Framework API], WINBIO_ASYNC_NOTIFY_CALLBACK, WINBIO_ASYNC_NOTIFY_MAXIMUM_VALUE, WINBIO_ASYNC_NOTIFY_MESSAGE, WINBIO_ASYNC_NOTIFY_NONE, secbiomet.winbio_async_notification_method, winbio/WINBIO_ASYNC_NOTIFICATION_METHOD, winbio/WINBIO_ASYNC_NOTIFY_CALLBACK, winbio/WINBIO_ASYNC_NOTIFY_MAXIMUM_VALUE, winbio/WINBIO_ASYNC_NOTIFY_MESSAGE, winbio/WINBIO_ASYNC_NOTIFY_NONE'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WINBIO_ASYNC_NOTIFICATION_METHOD, *PWINBIO_ASYNC_NOTIFICATION_METHOD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINBIO_ASYNC_NOTIFICATION_METHOD
 - winbio/_WINBIO_ASYNC_NOTIFICATION_METHOD
 - PWINBIO_ASYNC_NOTIFICATION_METHOD
 - winbio/PWINBIO_ASYNC_NOTIFICATION_METHOD
 - WINBIO_ASYNC_NOTIFICATION_METHOD
 - winbio/WINBIO_ASYNC_NOTIFICATION_METHOD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio.h
api_name:
 - WINBIO_ASYNC_NOTIFICATION_METHOD
---

# WINBIO_ASYNC_NOTIFICATION_METHOD enumeration


## -description

Defines constants that specify how completion notifications for asynchronous operations are to be delivered to the client application. This enumeration is used by the <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopenframework">WinBioAsyncOpenFramework</a> and <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a> functions.

## -enum-fields

### -field WINBIO_ASYNC_NOTIFY_NONE:0

The operation is synchronous.

### -field WINBIO_ASYNC_NOTIFY_CALLBACK

The client-implemented <a href="/windows/desktop/api/winbio/nc-winbio-pwinbio_async_completion_callback">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function is called by the framework.

### -field WINBIO_ASYNC_NOTIFY_MESSAGE

The framework sends completion notices to the client application window message queue.

### -field WINBIO_ASYNC_NOTIFY_MAXIMUM_VALUE

The maximum enumeration value. This constant is not directly used by the <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopenframework">WinBioAsyncOpenFramework</a> and <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>.

## -remarks

This enumeration was introduced in Windows 8.

## -see-also

<a href="/windows/desktop/SecBioMet/client-application-enumerations">Client Application Enumerations</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopenframework">WinBioAsyncOpenFramework</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>
