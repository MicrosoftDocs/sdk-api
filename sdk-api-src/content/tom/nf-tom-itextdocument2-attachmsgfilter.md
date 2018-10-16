---
UID: NF:tom.ITextDocument2.AttachMsgFilter
title: ITextDocument2::AttachMsgFilter
author: windows-sdk-content
description: Attaches a new message filter to the edit instance. All window messages that the edit instance receives are forwarded to the message filter.
old-location: controls\itextdocument2_attachmsgfilter.htm
tech.root: controls
ms.assetid: 055b9d59-59cc-4922-b6b9-920885969dbc
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: AttachMsgFilter, AttachMsgFilter method [Windows Controls], AttachMsgFilter method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],AttachMsgFilter method, ITextDocument2.AttachMsgFilter, ITextDocument2::AttachMsgFilter, controls.itextdocument2_attachmsgfilter, tom/ITextDocument2::AttachMsgFilter
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
 - ITextDocument2.AttachMsgFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument2::AttachMsgFilter


## -description


Attaches a new message filter to the edit instance. All window messages that the edit instance receives are forwarded to the message filter. 


## -parameters




### -param pFilter [in]

Type: <b>IUnknown*</b>

The message filter.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



 The message filter must be bound to the document before it can be used.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

