---
UID: NF:shobjidl.IUserNotification2.Show
title: IUserNotification2::Show method
author: windows-driver-content
description: Displays the user information in a balloon-style tooltip.
old-location: shell\IUserNotification2_Show.htm
old-project: shell
ms.assetid: 928e9a78-6976-4dcb-b01d-766561f6a861
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IUserNotification2, IUserNotification2 interface [Windows Shell], Show method, IUserNotification2::Show, Show method [Windows Shell], Show method [Windows Shell], IUserNotification2 interface, Show,IUserNotification2.Show, _shell_IUserNotification2_Show, shell.IUserNotification2_Show, shobjidl/IUserNotification2::Show
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
-	IUserNotification2.Show
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IUserNotification2::Show method


## -description


Displays the user information in a balloon-style tooltip.


## -parameters




### -param pqc [in, optional]

Type: <b><a href="https://msdn.microsoft.com/94dee6cc-a142-4180-a562-14f4ded16884">IQueryContinue</a>*</b>

An <a href="https://msdn.microsoft.com/94dee6cc-a142-4180-a562-14f4ded16884">IQueryContinue</a> interface pointer, used to determine whether the notification display can continue or should stop (for example, if the user closes the notification). This value can be <b>NULL</b>.


### -param dwContinuePollInterval [in]

Type: <b>DWORD</b>

The length of time, in milliseconds, to display user information.


### -param pSink [in]

Type: <b><a href="https://msdn.microsoft.com/f746a4d4-8649-43a1-ac9b-773402dfb6c7">IUserNotificationCallback</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/f746a4d4-8649-43a1-ac9b-773402dfb6c7">IUserNotificationCallback</a> interface, used to handle mouse click and hover actions on the notification area icon and within the notification itself. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6605a014-4f79-4856-8fd9-df926ea76052">IUserNotification2</a>



<a href="https://msdn.microsoft.com/1f908581-9635-4090-9e52-1dfb9a206d38">Show</a>
 

 

