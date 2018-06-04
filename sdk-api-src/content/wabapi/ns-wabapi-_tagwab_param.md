---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _tagWAB_PARAM structure


## -description


Do not use. Contains the input information to pass to <a href="https://msdn.microsoft.com/68f2dcd5-9153-488a-ab9b-7cc03b09a87f">WABOpen</a>.


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

Indicates that WAB is to use Outlook Express for e-mail before checking for a default Simple MAPI client. Default behaviour is to check for the Simple MAPI client first.



#### WAB_ENABLE_PROFILES (WAB_ENABLE_PROFILES)

Invokes WAB in an Identity-aware session using Identity-Manager based profiles. Available only on Internet Explorer 5 or later.


### -field guidPSExt

Type: <b>GUID</b>

Value of type <b>GUID</b> that specifies the GUID that identifies the calling application's property sheet extensions. The GUID can be used to determine whether the extension property sheets are displayed or not. Available only on Internet Explorer 5 or later.

