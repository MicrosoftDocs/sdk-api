---
UID: NF:control.IBasicVideo.IsUsingDefaultDestination
title: IBasicVideo::IsUsingDefaultDestination (control.h)
description: The IsUsingDefaultDestination method queries whether the renderer is using the default destination rectangle.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","IsUsingDefaultDestination method","IBasicVideo.IsUsingDefaultDestination","IBasicVideo::IsUsingDefaultDestination","IBasicVideoIsUsingDefaultDestination","IsUsingDefaultDestination","IsUsingDefaultDestination method [DirectShow]","IsUsingDefaultDestination method [DirectShow]","IBasicVideo interface","control/IBasicVideo::IsUsingDefaultDestination","dshow.ibasicvideo_isusingdefaultdestination"]
old-location: dshow\ibasicvideo_isusingdefaultdestination.htm
tech.root: dshow
ms.assetid: eceec24b-7743-4989-b112-e6a70283d397
ms.date: 12/05/2018
ms.keywords: IBasicVideo interface [DirectShow],IsUsingDefaultDestination method, IBasicVideo.IsUsingDefaultDestination, IBasicVideo::IsUsingDefaultDestination, IBasicVideoIsUsingDefaultDestination, IsUsingDefaultDestination, IsUsingDefaultDestination method [DirectShow], IsUsingDefaultDestination method [DirectShow],IBasicVideo interface, control/IBasicVideo::IsUsingDefaultDestination, dshow.ibasicvideo_isusingdefaultdestination
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBasicVideo::IsUsingDefaultDestination
 - control/IBasicVideo::IsUsingDefaultDestination
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IBasicVideo.IsUsingDefaultDestination
---

# IBasicVideo::IsUsingDefaultDestination


## -description

The <code>IsUsingDefaultDestination</code> method queries whether the renderer is using the default destination rectangle.



## -returns

Returns S_OK if the renderer is using the default destination rectangle, or S_FALSE otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>



<a href="/windows/desktop/api/control/nf-control-ibasicvideo-setdefaultdestinationposition">IBasicVideo::SetDefaultDestinationPosition</a>
