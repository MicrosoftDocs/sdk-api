---
UID: NF:tom.ITextDocument2.GetNotificationMode
title: ITextDocument2::GetNotificationMode method
author: windows-driver-content
description: Gets the notification mode.
old-location: controls\itextdocument2_getnotificationmode.htm
old-project: Controls
ms.assetid: 720f9759-96c1-45f0-9251-90d60532d247
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetNotificationMode method [Windows Controls], GetNotificationMode method [Windows Controls], ITextDocument2 interface, GetNotificationMode,ITextDocument2.GetNotificationMode, ITextDocument2, ITextDocument2 interface [Windows Controls], GetNotificationMode method, ITextDocument2::GetNotificationMode, controls.itextdocument2_getnotificationmode, tom/ITextDocument2::GetNotificationMode
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextDocument2.GetNotificationMode
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::GetNotificationMode method


## -description


Gets the notification mode.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The notification mode. This parameter is set to <b>tomTrue</b> if notifications are active, or <b>tomFalse</b> if not.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/b3dd9895-9fdd-4919-9e3a-382bb130f4b9">ITextDocument2::SetNotificationMode</a>
 

 

