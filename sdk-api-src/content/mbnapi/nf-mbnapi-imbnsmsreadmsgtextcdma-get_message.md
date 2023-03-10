---
UID: NF:mbnapi.IMbnSmsReadMsgTextCdma.get_Message
title: IMbnSmsReadMsgTextCdma::get_Message (mbnapi.h)
description: The contents of the message.
helpviewer_keywords: ["IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks]","Message property","IMbnSmsReadMsgTextCdma.Message","IMbnSmsReadMsgTextCdma.get_Message","IMbnSmsReadMsgTextCdma::Message","IMbnSmsReadMsgTextCdma::get_Message","Message property [Microsoft Broadband Networks]","Message property [Microsoft Broadband Networks]","IMbnSmsReadMsgTextCdma interface","get_Message","mbn.imbnsmsreadmsgtextcdma_message","mbnapi/IMbnSmsReadMsgTextCdma::Message","mbnapi/IMbnSmsReadMsgTextCdma::get_Message"]
old-location: mbn\imbnsmsreadmsgtextcdma_message.htm
tech.root: mbn
ms.assetid: 4ee67021-5c28-4f29-83fe-43387a4df5cc
ms.date: 12/05/2018
ms.keywords: IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks],Message property, IMbnSmsReadMsgTextCdma.Message, IMbnSmsReadMsgTextCdma.get_Message, IMbnSmsReadMsgTextCdma::Message, IMbnSmsReadMsgTextCdma::get_Message, Message property [Microsoft Broadband Networks], Message property [Microsoft Broadband Networks],IMbnSmsReadMsgTextCdma interface, get_Message, mbn.imbnsmsreadmsgtextcdma_message, mbnapi/IMbnSmsReadMsgTextCdma::Message, mbnapi/IMbnSmsReadMsgTextCdma::get_Message
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
 - IMbnSmsReadMsgTextCdma::get_Message
 - mbnapi/IMbnSmsReadMsgTextCdma::get_Message
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
 - IMbnSmsReadMsgTextCdma.Message
 - IMbnSmsReadMsgTextCdma.get_Message
---

# IMbnSmsReadMsgTextCdma::get_Message


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The contents of the message.

This property is read-only.

## -parameters

## -remarks

The maximum size of the message is specified by the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsmsconfiguration-get_cdmashortmsgsize">CdmaShortMsgSize</a> property of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsconfiguration">IMbnSmsConfiguration</a>  The size can also be no larger than <b>MBN_CDMA_SHORT_MSG_SIZE_MAX</b> (160).

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsreadmsgtextcdma">IMbnSmsReadMsgTextCdma</a>