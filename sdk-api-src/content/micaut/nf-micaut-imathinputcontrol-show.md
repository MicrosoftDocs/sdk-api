---
UID: NF:micaut.IMathInputControl.Show
title: IMathInputControl::Show (micaut.h)
author: windows-sdk-content
description: Shows the control.
old-location: tablet\imathinputcontrol_show.htm
tech.root: tablet
ms.assetid: d45d1e73-eace-4611-a4a4-28706a19766c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMathInputControl interface [Tablet PC],Show method, IMathInputControl.Show, IMathInputControl::Show, Show, Show method [Tablet PC], Show method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::Show, tablet.imathinputcontrol_show
ms.topic: method
f1_keywords: 
 - "micaut/IMathInputControl.Show"
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
 - IMathInputControl.Show
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMathInputControl::Show


## -description


Shows the control.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Shows the Math Input Control if it is not visible. If the control is already visible, puts the control on top of the z-order stack.
If <a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-setposition">SetPosition</a> is not called, <b>Show</b> will display the control at the top-left corner of the screen ((0, 0) in screen cooridnates). 
The control's width and height will be at their minimum.
	 


#### Examples


```

    HRESULT hr = CoInitialize(NULL);
    hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
    hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
    hr = g_spMIC->Show();  
    
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/creating-a-math-input-control">Creating a Math Input Control</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/customizing-the-math-input-control">Customizing the Math Input Control</a>



<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-hide">Hide</a>



<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>
 

 

