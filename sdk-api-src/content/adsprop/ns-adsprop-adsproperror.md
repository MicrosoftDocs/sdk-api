---
UID: NS:adsprop._ADSPROPERROR
title: ADSPROPERROR (adsprop.h)
description: The ADSPROPERROR structure is used to pass error data to the notification object with the ADsPropSendErrorMessage function or the WM_ADSPROP_NOTIFY_ERROR message.
helpviewer_keywords: ["*PADSPROPERROR","ADSPROPERROR","ADSPROPERROR structure [Active Directory]","PADSPROPERROR","PADSPROPERROR structure pointer [Active Directory]","_glines_adsproperror","ad.adsproperror","adsprop/ADSPROPERROR","adsprop/PADSPROPERROR"]
old-location: ad\adsproperror.htm
tech.root: ad
ms.assetid: 584cb3e7-3b26-4346-9162-b3e3064ded1a
ms.date: 12/05/2018
ms.keywords: '*PADSPROPERROR, ADSPROPERROR, ADSPROPERROR structure [Active Directory], PADSPROPERROR, PADSPROPERROR structure pointer [Active Directory], _glines_adsproperror, ad.adsproperror, adsprop/ADSPROPERROR, adsprop/PADSPROPERROR'
req.header: adsprop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: ADSPROPERROR, *PADSPROPERROR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ADSPROPERROR
 - adsprop/_ADSPROPERROR
 - PADSPROPERROR
 - adsprop/PADSPROPERROR
 - ADSPROPERROR
 - adsprop/ADSPROPERROR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Adsprop.h
api_name:
 - ADSPROPERROR
---

# ADSPROPERROR structure


## -description

The
  <b>ADSPROPERROR</b> structure is used to pass error
  data to the notification object with the <a href="/windows/desktop/api/adsprop/nf-adsprop-adspropsenderrormessage">ADsPropSendErrorMessage</a> function or the <a href="/windows/desktop/AD/wm-adsprop-notify-error">WM_ADSPROP_NOTIFY_ERROR</a> message.

## -struct-fields

### -field hwndPage

Contains the window handle of the property page that generated the error.

### -field pszPageTitle

Pointer to a NULL-terminated Unicode string that contains the title of the property page that generated the error.

### -field pszObjPath

Pointer to a NULL-terminated Unicode string that contains the ADsPath of the directory object that the error occurred on.

### -field pszObjClass

Pointer to a NULL-terminated Unicode string that contains the class name of the directory object that the error occurred on.

### -field hr

Contains an <b>HRESULT</b> value that specifies the  code of the error that occurred. If <i>hr</i> is not equal to <b>S_OK</b>, then <i>pszError</i> is ignored. If <i>hr</i> is equal to <b>S_OK</b>, then <i>pszError</i> contains an error message.

### -field pszError

Pointer to a NULL-terminated Unicode string that contains the error message to be displayed in the error dialog box. This member is ignored if <i>hr</i> is not equal to <b>S_OK</b>. In this case, the error dialog box will display a system-defined message for the error specified by <i>hr</i>.

## -see-also

<a href="/windows/desktop/api/adsprop/nf-adsprop-adspropsenderrormessage">ADsPropSendErrorMessage</a>



<a href="/windows/desktop/AD/wm-adsprop-notify-error">WM_ADSPROP_NOTIFY_ERROR</a>