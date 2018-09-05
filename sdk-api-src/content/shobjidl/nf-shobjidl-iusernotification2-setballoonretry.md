---
UID: NF:shobjidl.IUserNotification2.SetBalloonRetry
title: IUserNotification2::SetBalloonRetry
author: windows-sdk-content
description: Specifies the conditions for trying to display user information when the first attempt fails.
old-location: shell\IUserNotification2_SetBalloonRetry.htm
old-project: shell
ms.assetid: D6A72D9F-108F-4eaf-A867-F81C86C08809
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IUserNotification2 interface [Windows Shell],SetBalloonRetry method, IUserNotification2.SetBalloonRetry, IUserNotification2::SetBalloonRetry, SetBalloonRetry, SetBalloonRetry method [Windows Shell], SetBalloonRetry method [Windows Shell],IUserNotification2 interface, _shell_IUserNotification2_SetBalloonRetry, shell.IUserNotification2_SetBalloonRetry, shobjidl/IUserNotification2::SetBalloonRetry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IUserNotification2.SetBalloonRetry
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IUserNotification2::SetBalloonRetry


## -description


Specifies the conditions for trying to display user information when the first attempt fails.


## -parameters




### -param dwShowTime [in]

Type: <b>DWORD</b>

The amount of time, in milliseconds, to display the user information.


### -param dwInterval [in]

Type: <b>DWORD</b>

The interval of time, in milliseconds, between attempts to display the user information.


### -param cRetryCount [in]

Type: <b>UINT</b>

The number of times the system should try to display the user information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6605a014-4f79-4856-8fd9-df926ea76052">IUserNotification2</a>



<a href="https://msdn.microsoft.com/b9ad42e1-19eb-44a9-aa09-4a31840104d6">SetBalloonRetry</a>
 

 

