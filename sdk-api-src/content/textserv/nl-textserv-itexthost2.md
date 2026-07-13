---
UID: NL:textserv.ITextHost2
title: ITextHost2 (textserv.h)
description: The ITextHost2 interface extends the ITextHost interface.
helpviewer_keywords: ["ITextHost2","ITextHost2 interface [Windows Controls]","ITextHost2 interface [Windows Controls]","described","controls.itexthost2","textserv/ITextHost2"]
old-location: controls\itexthost2.htm
tech.root: Controls
ms.assetid: A715E70C-E8BB-4796-BDA6-90B745EC7761
ms.date: 12/05/2018
ms.keywords: ITextHost2, ITextHost2 interface [Windows Controls], ITextHost2 interface [Windows Controls],described, controls.itexthost2, textserv/ITextHost2
req.header: textserv.h
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
 - ITextHost2
 - textserv/ITextHost2
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
 - ITextHost2
---

# ITextHost2 class


## -description

The <b>ITextHost2</b> interface extends the <a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a> interface. The purpose of these interfaces, along with <a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a> and <a href="/windows/desktop/api/textserv/nl-textserv-itextservices2">ITextServices2</a>, is to enable rich edit controls to run without a dedicated window. The rich edit client typically has a window (<b>HWND</b>) that it shares with a number of windowless controls.

## -inheritance

The <b>ITextHost2</b> interface inherits from <a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>. <b>ITextHost2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>
