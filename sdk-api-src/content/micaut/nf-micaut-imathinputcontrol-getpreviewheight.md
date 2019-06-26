---
UID: NF:micaut.IMathInputControl.GetPreviewHeight
title: IMathInputControl::GetPreviewHeight (micaut.h)
author: windows-sdk-content
description: Retrieves the height in pixels of the preview area.
old-location: tablet\imathinputcontrol_getpreviewheight.htm
tech.root: tablet
ms.assetid: 3b3404f5-b775-483f-b3a9-9467c937226b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPreviewHeight, GetPreviewHeight method [Tablet PC], GetPreviewHeight method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],GetPreviewHeight method, IMathInputControl.GetPreviewHeight, IMathInputControl::GetPreviewHeight, micaut/IMathInputControl::GetPreviewHeight, tablet.imathinputcontrol_getpreviewheight
ms.topic: method
f1_keywords: 
 - "micaut/IMathInputControl.GetPreviewHeight"
req.header: micaut.h
req.include-header: Micaut.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Micaut.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - micaut.h
api_name:
 - IMathInputControl.GetPreviewHeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMathInputControl::GetPreviewHeight


## -description


Retrieves the height in pixels of the preview area.


## -parameters




### -param Height [out]

The height in pixels of the preview area.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Manually resizing the control can affect the height of the result-preview area. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/customizing-the-math-input-control">Customizing the Math Input Control</a>



<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-setpreviewheight">SetPreviewHeight</a>
 

 

