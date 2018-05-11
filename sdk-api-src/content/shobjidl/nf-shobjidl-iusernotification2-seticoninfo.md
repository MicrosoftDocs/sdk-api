---
UID: NF:shobjidl.IUserNotification2.SetIconInfo
title: IUserNotification2::SetIconInfo
author: windows-driver-content
description: Sets the notification area icon associated with specific user information.
old-location: shell\IUserNotification2_SetIconInfo.htm
old-project: shell
ms.assetid: 9A7B5891-6A0C-4302-89F7-07D985B0F185
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IUserNotification2 interface [Windows Shell],SetIconInfo method, IUserNotification2.SetIconInfo, IUserNotification2::SetIconInfo, SetIconInfo, SetIconInfo method [Windows Shell], SetIconInfo method [Windows Shell],IUserNotification2 interface, _shell_IUserNotification2_SetIconInfo, shell.IUserNotification2_SetIconInfo, shobjidl/IUserNotification2::SetIconInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	IUserNotification2.SetIconInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IUserNotification2::SetIconInfo


## -description


Sets the notification area icon associated with specific user information.


## -parameters




### -param hIcon [in]

Type: <b>HICON</b>

A handle to the icon.


### -param pszToolTip [in]

Type: <b>LPCWSTR</b>

A pointer to a string that contains the tooltip text to display for the specified icon. This value can be <b>NULL</b>, although it is not recommended.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6605a014-4f79-4856-8fd9-df926ea76052">IUserNotification2</a>



<a href="https://msdn.microsoft.com/f9a3612e-8a25-48d5-8122-44d6aa217bab">SetIconInfo</a>
 

 

