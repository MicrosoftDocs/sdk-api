---
UID: NN:mbnapi.IMbnSmsReadMsgTextCdma
title: IMbnSmsReadMsgTextCdma (mbnapi.h)
description: A collection of properties that represent a CDMA format SMS message read from the device memory.
helpviewer_keywords: ["IMbnSmsReadMsgTextCdma","IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks]","IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks]","described","mbn.imbnsmsreadmsgtextcdma","mbnapi/IMbnSmsReadMsgTextCdma"]
old-location: mbn\imbnsmsreadmsgtextcdma.htm
tech.root: mbn
ms.assetid: d26b09f7-eb83-46ed-82cb-a702d3af5d05
ms.date: 12/05/2018
ms.keywords: IMbnSmsReadMsgTextCdma, IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks], IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks],described, mbn.imbnsmsreadmsgtextcdma, mbnapi/IMbnSmsReadMsgTextCdma
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
 - IMbnSmsReadMsgTextCdma
 - mbnapi/IMbnSmsReadMsgTextCdma
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
 - IMbnSmsReadMsgTextCdma
---

# IMbnSmsReadMsgTextCdma interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

A collection of properties that represent a CDMA format SMS message read from the device memory.

## -remarks

This message format is valid only for CDMA devices and cannot be used with GSM devices.

 This interface is provided by the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsreadcomplete">OnSmsReadComplete</a> and <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsevents-onsmsnewclass0message">OnSmsNewClass0Message</a> methods of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsevents">IMbnSmsEvents</a> interface.