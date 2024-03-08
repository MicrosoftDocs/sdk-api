---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetHyperlinkNavigateUri
title: IXpsOMVisual::SetHyperlinkNavigateUri (xpsobjectmodel.h)
description: Sets the destination URI of the visual's hyperlink.
helpviewer_keywords: ["IXpsOMVisual interface [XPS Documents and Packaging]","SetHyperlinkNavigateUri method","IXpsOMVisual.SetHyperlinkNavigateUri","IXpsOMVisual::SetHyperlinkNavigateUri","SetHyperlinkNavigateUri","SetHyperlinkNavigateUri method [XPS Documents and Packaging]","SetHyperlinkNavigateUri method [XPS Documents and Packaging]","IXpsOMVisual interface","xps.ixpsomvisual_sethyperlinknavigateuri","xpsobjectmodel/IXpsOMVisual::SetHyperlinkNavigateUri"]
old-location: xps\ixpsomvisual_sethyperlinknavigateuri.htm
tech.root: xps
ms.assetid: 6909d287-67c8-4f01-8523-6011932d1d34
ms.date: 12/05/2018
ms.keywords: IXpsOMVisual interface [XPS Documents and Packaging],SetHyperlinkNavigateUri method, IXpsOMVisual.SetHyperlinkNavigateUri, IXpsOMVisual::SetHyperlinkNavigateUri, SetHyperlinkNavigateUri, SetHyperlinkNavigateUri method [XPS Documents and Packaging], SetHyperlinkNavigateUri method [XPS Documents and Packaging],IXpsOMVisual interface, xps.ixpsomvisual_sethyperlinknavigateuri, xpsobjectmodel/IXpsOMVisual::SetHyperlinkNavigateUri
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMVisual::SetHyperlinkNavigateUri
 - xpsobjectmodel/IXpsOMVisual::SetHyperlinkNavigateUri
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMVisual.SetHyperlinkNavigateUri
---

# IXpsOMVisual::SetHyperlinkNavigateUri


## -description

Sets the destination URI of the visual's hyperlink.

## -parameters

### -param hyperlinkUri [in]

The <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775038(v=vs.85)">IUri</a> interface that contains the destination URI of the visual's hyperlink.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Setting an object's URI makes the object a hyperlink. When activated or clicked, the object   will navigate to the destination that is  specified by the URI in <i>hyperlinkUri</i>.

## -see-also

<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775038(v=vs.85)">IUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>