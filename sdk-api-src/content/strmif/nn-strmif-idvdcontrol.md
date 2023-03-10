---
UID: NN:strmif.IDvdControl
title: IDvdControl (strmif.h)
description: Note  This interface has been deprecated. (IDvdControl)
helpviewer_keywords: ["IDvdControl","IDvdControl interface [DirectShow]","IDvdControl interface [DirectShow]","described","IDvdControlInterface","dshow.idvdcontrol","strmif/IDvdControl"]
old-location: dshow\idvdcontrol.htm
tech.root: dshow
ms.assetid: a6ca0fe8-84e3-43e6-9421-29dcff056dfd
ms.date: 12/05/2018
ms.keywords: IDvdControl, IDvdControl interface [DirectShow], IDvdControl interface [DirectShow],described, IDvdControlInterface, dshow.idvdcontrol, strmif/IDvdControl
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdControl
 - strmif/IDvdControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IDvdControl
---

# IDvdControl interface


## -description

<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a>.</div>
<div> </div>
The <code>IDvdControl</code> interface controls the playback and search mechanisms of a DVD title that contains one or more video movies. Use this interface to control playback (set root drive, play, stop, and so forth) or use DVD-specific functionality such as menus and buttons when playing DVD-Video files.

## -inheritance

The <b>IDvdControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
