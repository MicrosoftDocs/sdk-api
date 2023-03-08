---
UID: NN:oleidl.IDropSource
title: IDropSource (oleidl.h)
description: The IDropSource interface is one of the interfaces you implement to provide drag-and-drop operations in your application.
helpviewer_keywords: ["IDropSource","IDropSource interface [COM]","IDropSource interface [COM]","described","_ole_idropsource","com.idropsource","oleidl/IDropSource"]
old-location: com\idropsource.htm
tech.root: com
ms.assetid: 963a36bc-4ad7-4591-bffc-a96b4310177d
ms.date: 12/05/2018
ms.keywords: IDropSource, IDropSource interface [COM], IDropSource interface [COM],described, _ole_idropsource, com.idropsource, oleidl/IDropSource
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IDropSource
 - oleidl/IDropSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IDropSource
---

# IDropSource interface


## -description

The <b>IDropSource</b> interface is one of the interfaces you implement to provide drag-and-drop operations in your application. It contains methods used in any application used as a data source in a drag-and-drop operation. The data source application in a drag-and-drop operation is responsible for:
<ul>
<li>Determining the data being dragged based on the user's selection.</li>
<li>Initiating the drag-and-drop operation based on the user's mouse actions.</li>
<li>Generating some of the visual feedback during the drag-and-drop operation, such as setting the cursor and highlighting the data selected for the drag-and-drop operation.</li>
<li>Canceling or completing the drag-and-drop operation based on the user's mouse actions.</li>
<li>Performing any action on the original data caused by the drop operation, such as deleting the data on a drag move.</li>
</ul><b>IDropSource</b> contains the methods for generating visual feedback to the end user and for canceling or completing the drag-and-drop operation. You also need to call the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a>, <a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a>, and <a href="/windows/desktop/api/ole2/nf-ole2-revokedragdrop">RevokeDragDrop</a> functions in drag-and-drop operations.

## -inheritance

The <b>IDropSource</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDropSource</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsourcenotify">IDropSourceNotify</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>
