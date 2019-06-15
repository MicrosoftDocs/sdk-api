---
UID: NF:tom.ITextDocument2.SetIMEInProgress
title: ITextDocument2::SetIMEInProgress (tom.h)
author: windows-sdk-content
description: Sets the state of the Input Method Editor (IME) in-progress flag.
old-location: controls\itextdocument2_setimeinprogress.htm
tech.root: Controls
ms.assetid: 65db4e97-48c9-48e0-b436-2b2e6713bebd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetIMEInProgress method, ITextDocument2.SetIMEInProgress, ITextDocument2::SetIMEInProgress, SetIMEInProgress, SetIMEInProgress method [Windows Controls], SetIMEInProgress method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setimeinprogress, tom/ITextDocument2::SetIMEInProgress
ms.topic: method
f1_keywords: ["tom/ITextDocument2.SetIMEInProgress"]
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
 - ITextDocument2.SetIMEInProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextDocument2::SetIMEInProgress


## -description


Sets the state of the Input Method Editor (IME) in-progress flag.


## -parameters




### -param Value [in]

Type: <b>long</b>

Use <b>tomTrue</b> to turn  on the IME in-progress flag, or <b>tomFalse</b> to turn it off.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>
 

 

