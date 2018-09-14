---
UID: NS:winnetwk._REMOTE_NAME_INFOA
title: "_REMOTE_NAME_INFOA"
author: windows-sdk-content
description: The REMOTE_NAME_INFO structure contains information about the remote form of a universal name. It is used by the NPGetUniversalName function.
old-location: security\remote_name_info.htm
tech.root: secauthn
ms.assetid: 5dec0c40-757e-4c3b-8442-23f6d0f0e670
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: "*LPREMOTE_NAME_INFOA, LPREMOTE_NAME_INFO, LPREMOTE_NAME_INFO structure pointer [Security], REMOTE_NAME_INFO, REMOTE_NAME_INFO structure [Security], REMOTE_NAME_INFOA, REMOTE_NAME_INFOW, _REMOTE_NAME_INFOA, _mnp_remote_name_info, security.remote_name_info, winnetwk/LPREMOTE_NAME_INFO, winnetwk/REMOTE_NAME_INFO, winnetwk/REMOTE_NAME_INFOA, winnetwk/REMOTE_NAME_INFOW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: REMOTE_NAME_INFOA, *LPREMOTE_NAME_INFOA
req.redist: 
---

# _REMOTE_NAME_INFOA structure


## -description


The <b>REMOTE_NAME_INFO</b> structure contains information about the remote form of a universal name. It is used by the 
<a href="https://msdn.microsoft.com/976b5910-c34f-49fa-b25e-82bf607e33a9">NPGetUniversalName</a> function.


## -struct-fields




### -field lpUniversalName

Pointer to the universal name if the provider supports universal names. Otherwise, this points to <b>NULL</b>.


### -field lpConnectionName

Pointer to a string containing the remote name used to make the connection. This string does not have a trailing backslash.


### -field lpRemainingPath

Pointer to the remaining path that must to be concatenated to a drive letter after a connection is established by means of <b>lpConnectionName</b>, to refer to the object specified during the call to <a href="https://msdn.microsoft.com/976b5910-c34f-49fa-b25e-82bf607e33a9">NPGetUniversalName</a>. This string has a backslash at the start of the path.

