---
UID: NF:textserv.ITextHost2.TxFreeTextServicesNotification
title: ITextHost2::TxFreeTextServicesNotification (textserv.h)
description: Notifies the text host that text services have been freed.
helpviewer_keywords: ["ITextHost2 interface [Windows Controls]","TxFreeTextServicesNotification method","ITextHost2.TxFreeTextServicesNotification","ITextHost2::TxFreeTextServicesNotification","TxFreeTextServicesNotification","TxFreeTextServicesNotification method [Windows Controls]","TxFreeTextServicesNotification method [Windows Controls]","ITextHost2 interface","controls.itexthost2_txfreetextservicesnotification","textserv/ITextHost2::TxFreeTextServicesNotification"]
old-location: controls\itexthost2_txfreetextservicesnotification.htm
tech.root: Controls
ms.assetid: AD017B2A-C38E-4A55-AA31-84639BE87FA8
ms.date: 12/05/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxFreeTextServicesNotification method, ITextHost2.TxFreeTextServicesNotification, ITextHost2::TxFreeTextServicesNotification, TxFreeTextServicesNotification, TxFreeTextServicesNotification method [Windows Controls], TxFreeTextServicesNotification method [Windows Controls],ITextHost2 interface, controls.itexthost2_txfreetextservicesnotification, textserv/ITextHost2::TxFreeTextServicesNotification
req.header: textserv.h
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextHost2::TxFreeTextServicesNotification
 - textserv/ITextHost2::TxFreeTextServicesNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextHost2.TxFreeTextServicesNotification
---

# ITextHost2::TxFreeTextServicesNotification


## -description

Notifies the text host that text services have been freed.



## -remarks

If the text host hasn't received this notification when the text host is shutting down, the text host can tell text services to release its text host reference count.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost2">ITextHost2</a>
