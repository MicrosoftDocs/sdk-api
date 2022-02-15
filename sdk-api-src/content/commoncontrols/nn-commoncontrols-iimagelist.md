---
UID: NN:commoncontrols.IImageList
title: IImageList (commoncontrols.h)
description: Exposes methods that manipulate and interact with image lists.
helpviewer_keywords: ["IImageList","IImageList interface [Windows Controls]","IImageList interface [Windows Controls]","described","comctl_IImageList","comctl_IImageList_cpp","commoncontrols/IImageList","controls.IImageList","controls.comctl_IImageList"]
old-location: controls\IImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\iimagelist.htm
ms.date: 12/05/2018
ms.keywords: IImageList, IImageList interface [Windows Controls], IImageList interface [Windows Controls],described, comctl_IImageList, comctl_IImageList_cpp, commoncontrols/IImageList, controls.IImageList, controls.comctl_IImageList
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CommonControls.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImageList
 - commoncontrols/IImageList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList
---

# IImageList interface


## -description

Exposes methods that manipulate and interact with image lists.

            
        

To use <b>IImageList</b>, specify Comctl32.dll version 6 in the manifest. If you do not do this, Comctl32.dll version 5 will be used by default, with which <b>IImageList</b> could display unpredictable behavior. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.

## -inheritance

The <b>IImageList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IImageList</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Controls/image-lists">Image Lists</a>
