---
UID: NF:textserv.IRichEditUiaInformation.GetBoundaryRectangle
title: IRichEditUiaInformation::GetBoundaryRectangle (textserv.h)
description: Retrieves the bounding rectangle of a windowless rich edit control.
helpviewer_keywords: ["GetBoundaryRectangle","GetBoundaryRectangle method [Windows Controls]","GetBoundaryRectangle method [Windows Controls]","IRichEditUiaInformation interface","IRichEditUiaInformation interface [Windows Controls]","GetBoundaryRectangle method","IRichEditUiaInformation.GetBoundaryRectangle","IRichEditUiaInformation::GetBoundaryRectangle","controls.irichedituiainformation_getboundaryrectangle","textserv/IRichEditUiaInformation::GetBoundaryRectangle"]
old-location: controls\irichedituiainformation_getboundaryrectangle.htm
tech.root: Controls
ms.assetid: DCDE0730-25C4-4856-AC20-36C36E20AFB1
ms.date: 12/05/2018
ms.keywords: GetBoundaryRectangle, GetBoundaryRectangle method [Windows Controls], GetBoundaryRectangle method [Windows Controls],IRichEditUiaInformation interface, IRichEditUiaInformation interface [Windows Controls],GetBoundaryRectangle method, IRichEditUiaInformation.GetBoundaryRectangle, IRichEditUiaInformation::GetBoundaryRectangle, controls.irichedituiainformation_getboundaryrectangle, textserv/IRichEditUiaInformation::GetBoundaryRectangle
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
 - IRichEditUiaInformation::GetBoundaryRectangle
 - textserv/IRichEditUiaInformation::GetBoundaryRectangle
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
 - IRichEditUiaInformation.GetBoundaryRectangle
---

# IRichEditUiaInformation::GetBoundaryRectangle


## -description

Retrieves the bounding rectangle of a windowless rich edit control.

## -parameters

### -param pUiaRect

Type: <b>UiaRect*</b>

The bounding rectangle, in screen coordinates.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/textserv/nn-textserv-irichedituiainformation">IRichEditUiaInformation</a>