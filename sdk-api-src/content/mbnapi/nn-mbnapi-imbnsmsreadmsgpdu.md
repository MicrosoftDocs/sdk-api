---
UID: NN:mbnapi.IMbnSmsReadMsgPdu
title: IMbnSmsReadMsgPdu (mbnapi.h)
description: A collection of properties that represent an SMS message read from the device memory.
helpviewer_keywords: ["IMbnSmsReadMsgPdu","IMbnSmsReadMsgPdu interface [Microsoft Broadband Networks]","IMbnSmsReadMsgPdu interface [Microsoft Broadband Networks]","described","mbn.imbnsmsreadmsgpdu","mbnapi/IMbnSmsReadMsgPdu"]
old-location: mbn\imbnsmsreadmsgpdu.htm
tech.root: mbn
ms.assetid: dc0e15c4-6203-4105-9d19-5931b27047d2
ms.date: 12/05/2018
ms.keywords: IMbnSmsReadMsgPdu, IMbnSmsReadMsgPdu interface [Microsoft Broadband Networks], IMbnSmsReadMsgPdu interface [Microsoft Broadband Networks],described, mbn.imbnsmsreadmsgpdu, mbnapi/IMbnSmsReadMsgPdu
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
 - IMbnSmsReadMsgPdu
 - mbnapi/IMbnSmsReadMsgPdu
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
 - IMbnSmsReadMsgPdu
---

# IMbnSmsReadMsgPdu interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

A collection of properties that represent an SMS message read from the device memory.

## -remarks

This interface is provided by the 
     <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsreadcomplete">OnSmsReadComplete</a> and 
     <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsnewclass0message">OnSmsNewClass0Message</a> methods of the 
     <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a> interface.