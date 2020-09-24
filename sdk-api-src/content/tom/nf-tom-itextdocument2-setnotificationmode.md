---
UID: NF:tom.ITextDocument2.SetNotificationMode
title: ITextDocument2::SetNotificationMode (tom.h)
description: Sets the notification mode.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","SetNotificationMode method","ITextDocument2.SetNotificationMode","ITextDocument2::SetNotificationMode","SetNotificationMode","SetNotificationMode method [Windows Controls]","SetNotificationMode method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_setnotificationmode","tom/ITextDocument2::SetNotificationMode"]
old-location: controls\itextdocument2_setnotificationmode.htm
tech.root: Controls
ms.assetid: b3dd9895-9fdd-4919-9e3a-382bb130f4b9
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetNotificationMode method, ITextDocument2.SetNotificationMode, ITextDocument2::SetNotificationMode, SetNotificationMode, SetNotificationMode method [Windows Controls], SetNotificationMode method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setnotificationmode, tom/ITextDocument2::SetNotificationMode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextDocument2::SetNotificationMode
 - tom/ITextDocument2::SetNotificationMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument2.SetNotificationMode
---

# ITextDocument2::SetNotificationMode


## -description

Sets the notification mode.

## -parameters

### -param Value [in]

Type: <b>long</b>

The notification mode. Use <b>tomTrue</b> to turn on notifications, or  <b>tomFalse</b> to turn them off.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getnotificationmode">ITextDocument2::GetNotificationMode</a>