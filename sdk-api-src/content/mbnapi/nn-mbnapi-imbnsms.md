---
UID: NN:mbnapi.IMbnSms
title: IMbnSms (mbnapi.h)
description: SMS interface for sending and receiving messages as well as controlling the messaging configuration.
helpviewer_keywords: ["IMbnSms","IMbnSms interface [Microsoft Broadband Networks]","IMbnSms interface [Microsoft Broadband Networks]","described","mbn.imbnsms","mbnapi/IMbnSms"]
old-location: mbn\imbnsms.htm
tech.root: mbn
ms.assetid: 4a5fae5a-91d5-4a94-ac54-cb641147e8dc
ms.date: 12/05/2018
ms.keywords: IMbnSms, IMbnSms interface [Microsoft Broadband Networks], IMbnSms interface [Microsoft Broadband Networks],described, mbn.imbnsms, mbnapi/IMbnSms
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
 - IMbnSms
 - mbnapi/IMbnSms
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
 - IMbnSms
---

# IMbnSms interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

SMS interface for sending and receiving messages as well as controlling the messaging configuration.

## -inheritance

The <b>IMbnSms</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnSms</b> also has these types of members:

## -remarks

The calling application can acquire this interface by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>
