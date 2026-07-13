---
UID: NS:winnetwk._REMOTE_NAME_INFOW
title: REMOTE_NAME_INFOW (winnetwk.h)
description: The REMOTE_NAME_INFO structure contains information about the remote form of a universal name. It is used by the NPGetUniversalName function. (Unicode)
helpviewer_keywords: ["*LPREMOTE_NAME_INFOW","LPREMOTE_NAME_INFO","LPREMOTE_NAME_INFO structure pointer [Security]","REMOTE_NAME_INFO","REMOTE_NAME_INFO structure [Security]","REMOTE_NAME_INFOA","REMOTE_NAME_INFOW","_mnp_remote_name_info","security.remote_name_info","winnetwk/LPREMOTE_NAME_INFO","winnetwk/REMOTE_NAME_INFO","winnetwk/REMOTE_NAME_INFOA","winnetwk/REMOTE_NAME_INFOW"]
old-location: security\remote_name_info.htm
tech.root: security
ms.assetid: 5dec0c40-757e-4c3b-8442-23f6d0f0e670
ms.date: 12/05/2018
ms.keywords: '*LPREMOTE_NAME_INFOW, LPREMOTE_NAME_INFO, LPREMOTE_NAME_INFO structure pointer [Security], REMOTE_NAME_INFO, REMOTE_NAME_INFO structure [Security], REMOTE_NAME_INFOA, REMOTE_NAME_INFOW, _mnp_remote_name_info, security.remote_name_info, winnetwk/LPREMOTE_NAME_INFO, winnetwk/REMOTE_NAME_INFO, winnetwk/REMOTE_NAME_INFOA, winnetwk/REMOTE_NAME_INFOW'
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: REMOTE_NAME_INFOW (Unicode) and REMOTE_NAME_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: REMOTE_NAME_INFOW, *LPREMOTE_NAME_INFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _REMOTE_NAME_INFOW
 - winnetwk/_REMOTE_NAME_INFOW
 - LPREMOTE_NAME_INFOW
 - winnetwk/LPREMOTE_NAME_INFOW
 - REMOTE_NAME_INFOW
 - winnetwk/REMOTE_NAME_INFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnetwk.h
api_name:
 - REMOTE_NAME_INFO
 - REMOTE_NAME_INFOA
 - REMOTE_NAME_INFOW
---

# REMOTE_NAME_INFOW structure


## -description

The <b>REMOTE_NAME_INFO</b> structure contains information about the remote form of a universal name. It is used by the 
<a href="/windows/desktop/api/npapi/nf-npapi-npgetuniversalname">NPGetUniversalName</a> function.

## -struct-fields

### -field lpUniversalName

Pointer to the universal name if the provider supports universal names. Otherwise, this points to <b>NULL</b>.

### -field lpConnectionName

Pointer to a string containing the remote name used to make the connection. This string does not have a trailing backslash.

### -field lpRemainingPath

Pointer to the remaining path that must to be concatenated to a drive letter after a connection is established by means of <b>lpConnectionName</b>, to refer to the object specified during the call to <a href="/windows/desktop/api/npapi/nf-npapi-npgetuniversalname">NPGetUniversalName</a>. This string has a backslash at the start of the path.

## -remarks

> [!NOTE]
> The winnetwk.h header defines REMOTE_NAME_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
