---
UID: NF:micaut.IMathInputControl.GetPreviewHeight
title: IMathInputControl::GetPreviewHeight
author: windows-sdk-content
description: Retrieves the height in pixels of the preview area.
old-location: tablet\imathinputcontrol_getpreviewheight.htm
old-project: tablet
ms.assetid: 3b3404f5-b775-483f-b3a9-9467c937226b
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: GetPreviewHeight, GetPreviewHeight method [Tablet PC], GetPreviewHeight method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],GetPreviewHeight method, IMathInputControl.GetPreviewHeight, IMathInputControl::GetPreviewHeight, micaut/IMathInputControl::GetPreviewHeight, tablet.imathinputcontrol_getpreviewheight
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/922562be-4d5b-45b6-ad0b-49176f893c8e">Customizing the Math Input Control</a>



<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>



<a href="https://msdn.microsoft.com/a5e011f6-cd51-4016-ba15-c47c152bfa99">SetPreviewHeight</a>
 

 

