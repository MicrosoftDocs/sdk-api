---
UID: NS:wabapi._tagWAB_PARAM
title: WAB_PARAM (wabapi.h)
description: Do not use. Contains the input information to pass to WABOpen.
helpviewer_keywords: ["*LPWAB_PARAM","LPWAB_PARAM","LPWAB_PARAM structure pointer [Windows Address Book]","WAB_ENABLE_PROFILES","WAB_PARAM","WAB_PARAM structure [Windows Address Book]","WAB_USE_OE_SENDMAIL","_wab_WAB_PARAM","wab._wab_WAB_PARAM","wabapi/LPWAB_PARAM","wabapi/WAB_PARAM"]
old-location: wab\_wab_WAB_PARAM.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\wab_param.htm
ms.date: 12/05/2018
ms.keywords: '*LPWAB_PARAM, LPWAB_PARAM, LPWAB_PARAM structure pointer [Windows Address Book], WAB_ENABLE_PROFILES, WAB_PARAM, WAB_PARAM structure [Windows Address Book], WAB_USE_OE_SENDMAIL, _wab_WAB_PARAM, wab._wab_WAB_PARAM, wabapi/LPWAB_PARAM, wabapi/WAB_PARAM'
req.header: wabapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WAB_PARAM, *LPWAB_PARAM
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _tagWAB_PARAM
 - wabapi/_tagWAB_PARAM
 - LPWAB_PARAM
 - wabapi/LPWAB_PARAM
 - WAB_PARAM
 - wabapi/WAB_PARAM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabapi.h
api_name:
 - WAB_PARAM
---

# WAB_PARAM structure


## -description

Do not use. Contains the input information to pass to <a href="/previous-versions/windows/desktop/api/wabapi/nc-wabapi-wabopen">WABOpen</a>.

## -struct-fields

### -field cbSize

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies the size of the <b>WAB_PARAM</b> structure in bytes.

### -field hwnd

Type: <b>HWND</b>

Value of type <b>HWND</b> that specifies the window handle of the calling client application. Can be <b>NULL</b>.

### -field szFileName

Type: <b>LPTSTR</b>

Value of type <b>LPTSTR</b> that specifies the WAB file name to open. If this parameter is <b>NULL</b>, the default Address Book file is opened.

### -field ulFlags

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies flags that control the behavior of WAB functionality. Available only on Internet Explorer 4.0 or later.



#### WAB_USE_OE_SENDMAIL (WAB_USE_OE_SENDMAIL)

Indicates that WAB is to use Outlook Express for e-mail before checking for a default Simple MAPI client. Default behavior is to check for the Simple MAPI client first.



#### WAB_ENABLE_PROFILES (WAB_ENABLE_PROFILES)

Invokes WAB in an Identity-aware session using Identity-Manager based profiles. Available only on Internet Explorer 5 or later.

### -field guidPSExt

Type: <b>GUID</b>

Value of type <b>GUID</b> that specifies the GUID that identifies the calling application's property sheet extensions. The GUID can be used to determine whether the extension property sheets are displayed or not. Available only on Internet Explorer 5 or later.