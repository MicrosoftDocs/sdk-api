---
UID: NN:msinkaut.IInkCursorButtons
title: IInkCursorButtons (msinkaut.h)
description: Represents a collection of IInkCursorButton objects for an IInkCursor interface.
helpviewer_keywords: ["3f695ab4-8174-402f-b7d6-810f149f5153","IInkCursorButtons","IInkCursorButtons interface [Tablet PC]","IInkCursorButtons interface [Tablet PC]","described","msinkaut/IInkCursorButtons","tablet.iinkcursorbuttons"]
old-location: tablet\iinkcursorbuttons.htm
tech.root: tablet
ms.assetid: 3f695ab4-8174-402f-b7d6-810f149f5153
ms.date: 12/05/2018
ms.keywords: 3f695ab4-8174-402f-b7d6-810f149f5153, IInkCursorButtons, IInkCursorButtons interface [Tablet PC], IInkCursorButtons interface [Tablet PC],described, msinkaut/IInkCursorButtons, tablet.iinkcursorbuttons
req.header: msinkaut.h
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkCursorButtons
 - msinkaut/IInkCursorButtons
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkCursorButtons
 - IInkCursorButtons._NewEnum
---

# IInkCursorButtons interface


## -description

Represents a collection of <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton</a> objects for an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> interface.

## -inheritance

The <b>IInkCursorButtons</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkCursorButtons</b> also has these types of members:

## -remarks

You can use this collection to enumerate over the available <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton</a> objects on a known <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> object.

For more information about collections in COM, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC APIs.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton Interface</a>
