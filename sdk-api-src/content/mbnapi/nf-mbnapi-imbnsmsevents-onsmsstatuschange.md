---
UID: NF:mbnapi.IMbnSmsEvents.OnSmsStatusChange
title: IMbnSmsEvents::OnSmsStatusChange (mbnapi.h)
description: Notification method indicating a change in the status of the message store.
helpviewer_keywords: ["IMbnSmsEvents interface [Microsoft Broadband Networks]","OnSmsStatusChange method","IMbnSmsEvents.OnSmsStatusChange","IMbnSmsEvents::OnSmsStatusChange","OnSmsStatusChange","OnSmsStatusChange method [Microsoft Broadband Networks]","OnSmsStatusChange method [Microsoft Broadband Networks]","IMbnSmsEvents interface","mbn.imbnsmsevents_onsmsstatuschange","mbnapi/IMbnSmsEvents::OnSmsStatusChange"]
old-location: mbn\imbnsmsevents_onsmsstatuschange.htm
tech.root: mbn
ms.assetid: 8a3027e2-f8ee-476a-96e2-29ef4d87db38
ms.date: 12/05/2018
ms.keywords: IMbnSmsEvents interface [Microsoft Broadband Networks],OnSmsStatusChange method, IMbnSmsEvents.OnSmsStatusChange, IMbnSmsEvents::OnSmsStatusChange, OnSmsStatusChange, OnSmsStatusChange method [Microsoft Broadband Networks], OnSmsStatusChange method [Microsoft Broadband Networks],IMbnSmsEvents interface, mbn.imbnsmsevents_onsmsstatuschange, mbnapi/IMbnSmsEvents::OnSmsStatusChange
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - IMbnSmsEvents::OnSmsStatusChange
 - mbnapi/IMbnSmsEvents::OnSmsStatusChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnSmsEvents.OnSmsStatusChange
---

# IMbnSmsEvents::OnSmsStatusChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method indicating  a change in the status of the message store.

## -parameters

### -param sms [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a> interface representing the Mobile Broadband device for which the message store status has changed.

## -returns

This method must return <b>S_OK</b>.

## -remarks

An application can use the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a> interface to get the new status information.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a>