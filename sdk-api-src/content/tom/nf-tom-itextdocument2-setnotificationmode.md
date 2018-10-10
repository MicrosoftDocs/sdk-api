---
UID: NF:tom.ITextDocument2.SetNotificationMode
title: ITextDocument2::SetNotificationMode
author: windows-sdk-content
description: Sets the notification mode.
old-location: controls\itextdocument2_setnotificationmode.htm
tech.root: Controls
ms.assetid: b3dd9895-9fdd-4919-9e3a-382bb130f4b9
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetNotificationMode method, ITextDocument2.SetNotificationMode, ITextDocument2::SetNotificationMode, SetNotificationMode, SetNotificationMode method [Windows Controls], SetNotificationMode method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setnotificationmode, tom/ITextDocument2::SetNotificationMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument2.SetNotificationMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument2::SetNotificationMode


## -description


Sets the notification mode.


## -parameters




### -param Value [in]

Type: <b>long</b>

The notification mode. Use <b>tomTrue</b> to turn on notifications, or  <b>tomFalse</b> to turn them off.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/720f9759-96c1-45f0-9251-90d60532d247">ITextDocument2::GetNotificationMode</a>
 

 

