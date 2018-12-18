---
UID: NF:micaut.IMathInputControl.SetCustomPaint
title: IMathInputControl::SetCustomPaint
author: windows-sdk-content
description: Determines whether a button or background has custom painting.
old-location: tablet\imathinputcontrol_setcustompaint.htm
tech.root: tablet
ms.assetid: f734b73c-88a9-45d0-a657-ff048d1f5ffe
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMathInputControl interface [Tablet PC],SetCustomPaint method, IMathInputControl.SetCustomPaint, IMathInputControl::SetCustomPaint, SetCustomPaint, SetCustomPaint method [Tablet PC], SetCustomPaint method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::SetCustomPaint, tablet.imathinputcontrol_setcustompaint
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
 - IMathInputControl.SetCustomPaint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMathInputControl::SetCustomPaint


## -description


Determines whether a button or background has custom painting.


## -parameters




### -param Element [in]

The identifier for a button or background.


### -param Paint [in]

<b>VARIANT_TRUE</b> to enable custom painting for the specified UI element; otherwise, <b>VARIANT_FALSE</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If custom painting is enabled, the button or background will be rendered at least partially—and possibly completely—by the container.




## -see-also




<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>
 

 

