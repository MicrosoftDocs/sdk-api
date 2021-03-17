---
UID: NF:tom.ITextDocument2.AttachMsgFilter
title: ITextDocument2::AttachMsgFilter (tom.h)
description: Attaches a new message filter to the edit instance. All window messages that the edit instance receives are forwarded to the message filter.
helpviewer_keywords: ["AttachMsgFilter","AttachMsgFilter method [Windows Controls]","AttachMsgFilter method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","AttachMsgFilter method","ITextDocument2.AttachMsgFilter","ITextDocument2::AttachMsgFilter","controls.itextdocument2_attachmsgfilter","tom/ITextDocument2::AttachMsgFilter"]
old-location: controls\itextdocument2_attachmsgfilter.htm
tech.root: Controls
ms.assetid: 055b9d59-59cc-4922-b6b9-920885969dbc
ms.date: 12/05/2018
ms.keywords: AttachMsgFilter, AttachMsgFilter method [Windows Controls], AttachMsgFilter method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],AttachMsgFilter method, ITextDocument2.AttachMsgFilter, ITextDocument2::AttachMsgFilter, controls.itextdocument2_attachmsgfilter, tom/ITextDocument2::AttachMsgFilter
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
 - ITextDocument2::AttachMsgFilter
 - tom/ITextDocument2::AttachMsgFilter
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
 - ITextDocument2.AttachMsgFilter
---

# ITextDocument2::AttachMsgFilter


## -description

Attaches a new message filter to the edit instance. All window messages that the edit instance receives are forwarded to the message filter.

## -parameters

### -param pFilter [in]

Type: <b>IUnknown*</b>

The message filter.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 The message filter must be bound to the document before it can be used.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>