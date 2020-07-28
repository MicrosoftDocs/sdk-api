---
UID: NF:tom.ITextDocument2.GetNotificationMode
title: ITextDocument2::GetNotificationMode (tom.h)
description: Gets the notification mode.
helpviewer_keywords: ["GetNotificationMode","GetNotificationMode method [Windows Controls]","GetNotificationMode method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetNotificationMode method","ITextDocument2.GetNotificationMode","ITextDocument2::GetNotificationMode","controls.itextdocument2_getnotificationmode","tom/ITextDocument2::GetNotificationMode"]
old-location: controls\itextdocument2_getnotificationmode.htm
tech.root: Controls
ms.assetid: 720f9759-96c1-45f0-9251-90d60532d247
ms.date: 12/05/2018
ms.keywords: GetNotificationMode, GetNotificationMode method [Windows Controls], GetNotificationMode method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetNotificationMode method, ITextDocument2.GetNotificationMode, ITextDocument2::GetNotificationMode, controls.itextdocument2_getnotificationmode, tom/ITextDocument2::GetNotificationMode
f1_keywords:
- tom/ITextDocument2.GetNotificationMode
dev_langs:
- c++
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
- ITextDocument2.GetNotificationMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextDocument2::GetNotificationMode


## -description


Gets the notification mode.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The notification mode. This parameter is set to <b>tomTrue</b> if notifications are active, or <b>tomFalse</b> if not.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-setnotificationmode">ITextDocument2::SetNotificationMode</a>
 

 

