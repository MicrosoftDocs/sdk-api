---
UID: NN:mbnapi.IMbnSmsConfiguration
title: IMbnSmsConfiguration (mbnapi.h)
description: Provides access to the SMS configuration of a device.
helpviewer_keywords: ["IMbnSmsConfiguration","IMbnSmsConfiguration interface [Microsoft Broadband Networks]","IMbnSmsConfiguration interface [Microsoft Broadband Networks]","described","mbn.imbnsmsconfiguration","mbnapi/IMbnSmsConfiguration"]
old-location: mbn\imbnsmsconfiguration.htm
tech.root: mbn
ms.assetid: ee261c32-aa17-496a-a568-d9da43e1e23a
ms.date: 12/05/2018
ms.keywords: IMbnSmsConfiguration, IMbnSmsConfiguration interface [Microsoft Broadband Networks], IMbnSmsConfiguration interface [Microsoft Broadband Networks],described, mbn.imbnsmsconfiguration, mbnapi/IMbnSmsConfiguration
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
 - IMbnSmsConfiguration
 - mbnapi/IMbnSmsConfiguration
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
 - IMbnSmsConfiguration
---

# IMbnSmsConfiguration interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Provides access to the SMS configuration of a device.

## -remarks

This interface is acquired by a call to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsms-getsmsconfiguration">GetSmsConfiguration</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsms">IMbnSms</a> interface.