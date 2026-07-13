---
UID: NN:msinkaut15.IInkDivisionUnits
title: IInkDivisionUnits (msinkaut15.h)
description: Contains a collection of IInkDivisionUnit objects that are contained in an IInkDivisionResult object.
helpviewer_keywords: ["IInkDivisionUnits","IInkDivisionUnits interface [Tablet PC]","IInkDivisionUnits interface [Tablet PC]","described","efce8756-f42b-4d9a-bfed-4297e7e0fdec","msinkaut15/IInkDivisionUnits","tablet.iinkdivisionunits"]
old-location: tablet\iinkdivisionunits.htm
tech.root: tablet
ms.assetid: efce8756-f42b-4d9a-bfed-4297e7e0fdec
ms.date: 12/05/2018
ms.keywords: IInkDivisionUnits, IInkDivisionUnits interface [Tablet PC], IInkDivisionUnits interface [Tablet PC],described, efce8756-f42b-4d9a-bfed-4297e7e0fdec, msinkaut15/IInkDivisionUnits, tablet.iinkdivisionunits
req.header: msinkaut15.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDivisionUnits
 - msinkaut15/IInkDivisionUnits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inkdiv.dll
 - Inkdiv.dll.dll
api_name:
 - IInkDivisionUnits
 - IInkDivisionUnits._NewEnum
---

# IInkDivisionUnits interface


## -description

Contains a collection of <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit</a> objects that are contained in an <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult</a> object.

## -inheritance

The <b>IInkDivisionUnits</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkDivisionUnits</b> also has these types of members:

## -remarks

The <a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype">ResultByType</a> method of the <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult</a> object returns the requested structural elements of the analysis results in a <b>DivisionUnits</b> collection.

For more information about collections in Automation, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult">IInkDivisionResult Interface</a>



<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit Interface</a>
