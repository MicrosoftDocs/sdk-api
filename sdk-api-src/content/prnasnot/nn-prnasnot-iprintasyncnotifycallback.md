---
UID: NN:prnasnot.IPrintAsyncNotifyCallback
title: IPrintAsyncNotifyCallback (prnasnot.h)
description: Creates and manages a communication channel used by applications and components that are hosted by the print spooler.
helpviewer_keywords: ["IPrintAsyncNotifyCallback","IPrintAsyncNotifyCallback interface [Windows GDI]","IPrintAsyncNotifyCallback interface [Windows GDI]","described","_win32_IPrintAsyncNotifyCallback","gdi.iprintasyncnotifycallback","prnasnot/IPrintAsyncNotifyCallback"]
old-location: gdi\iprintasyncnotifycallback.htm
tech.root: xps
ms.assetid: e2b021cd-1cfd-42b7-b6e4-7f8671b013f6
ms.date: 12/05/2018
ms.keywords: IPrintAsyncNotifyCallback, IPrintAsyncNotifyCallback interface [Windows GDI], IPrintAsyncNotifyCallback interface [Windows GDI],described, _win32_IPrintAsyncNotifyCallback, gdi.iprintasyncnotifycallback, prnasnot/IPrintAsyncNotifyCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPrintAsyncNotifyCallback
 - prnasnot/IPrintAsyncNotifyCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.h
api_name:
 - IPrintAsyncNotifyCallback
---

# IPrintAsyncNotifyCallback interface


## -description

Creates and manages a communication channel used by applications and components that are hosted by the print spooler.

## -inheritance

The <b>IPrintAsyncNotifyCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPrintAsyncNotifyCallback</b> also has these types of members:

## -remarks

For an application to receive notifications from a Print Spooler-hosted component, it must provide an <b>IPrintAsyncNotifyCallback</b> object when it registers for notifications.

A Print Spooler-hosted component that opens a bidirectional communication channel with a listening application must provide an <b>IPrintAsyncNotifyCallback</b> object.

## -see-also

<a href="/windows/desktop/printdocs/asynchronous-notification-interfaces">Asynchronous Printing Notification Interfaces</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>
