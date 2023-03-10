---
UID: NS:mbnapi.MBN_SMS_FILTER
title: MBN_SMS_FILTER (mbnapi.h)
description: The MBN_SMS_FILTER structure contains the values that describe a set of SMS messages.
helpviewer_keywords: ["MBN_SMS_FILTER","MBN_SMS_FILTER structure [Microsoft Broadband Networks]","mbn.mbn_sms_filter","mbnapi/MBN_SMS_FILTER"]
old-location: mbn\mbn_sms_filter.htm
tech.root: mbn
ms.assetid: f8dffd7b-3c12-43da-b61c-3c9aa8f1136f
ms.date: 12/05/2018
ms.keywords: MBN_SMS_FILTER, MBN_SMS_FILTER structure [Microsoft Broadband Networks], mbn.mbn_sms_filter, mbnapi/MBN_SMS_FILTER
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
req.typenames: MBN_SMS_FILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_SMS_FILTER
 - mbnapi/MBN_SMS_FILTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_SMS_FILTER
---

# MBN_SMS_FILTER structure


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_SMS_FILTER</b> structure contains the values that describe a set of SMS messages.

## -struct-fields

### -field flag

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_sms_flag">MBN_SMS_FLAG</a> value that 	specifies the message class.

### -field messageIndex

Contains the index of a particular message in device memory.  This value is only meaningful when <b>flag</b> is set to 	<b>MBN_SMS_FLAG_INDEX</b>.  The maximum range of this value is from 1 to the <a href="/previous-versions/windows/desktop/legacy/dd323170(v=vs.85)">MaxMessageIndex</a> property of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsconfiguration">IMbnSmsConfiguration</a>.