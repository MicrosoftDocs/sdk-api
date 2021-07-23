---
UID: NF:micaut.IMathInputControl.EnableExtendedButtons
title: IMathInputControl::EnableExtendedButtons (micaut.h)
description: Determines whether the extended set of control buttons is shown.
helpviewer_keywords: ["EnableExtendedButtons","EnableExtendedButtons method [Tablet PC]","EnableExtendedButtons method [Tablet PC]","IMathInputControl interface","IMathInputControl interface [Tablet PC]","EnableExtendedButtons method","IMathInputControl.EnableExtendedButtons","IMathInputControl::EnableExtendedButtons","micaut/IMathInputControl::EnableExtendedButtons","tablet.imathinputcontrol_enableextendedbuttons"]
old-location: tablet\imathinputcontrol_enableextendedbuttons.htm
tech.root: tablet
ms.assetid: e8cdae54-ff0b-4361-bd38-1b99137736ab
ms.date: 12/05/2018
ms.keywords: EnableExtendedButtons, EnableExtendedButtons method [Tablet PC], EnableExtendedButtons method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],EnableExtendedButtons method, IMathInputControl.EnableExtendedButtons, IMathInputControl::EnableExtendedButtons, micaut/IMathInputControl::EnableExtendedButtons, tablet.imathinputcontrol_enableextendedbuttons
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMathInputControl::EnableExtendedButtons
 - micaut/IMathInputControl::EnableExtendedButtons
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - micaut.h
api_name:
 - IMathInputControl.EnableExtendedButtons
---

# IMathInputControl::EnableExtendedButtons


## -description

Determines whether the extended set of control buttons is shown.

## -parameters

### -param Extended [in]

<b>VARIANT_TRUE</b> to show the extended button set; <b>VARIANT_FALSE</b> to show the basic button set.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The basic button set is shown by default.

The basic button set contains the <b>Clear</b>, <b>Erase</b>, <b>Insert</b>, <b>Select and Correct</b>, and <b>Write</b> buttons. The extended button set contains the basic set plus the <b>Redo</b> and <b>Undo</b> buttons.

The following image shows the Math Input Control with extended buttons enabled.



<img alt="Math input control with extended buttons enabled" src="./images/MIC.png"/>
The following image shows the Math Input Control with extended buttons disabled.



<img alt="Math input control with extended buttons disabled" src="./images/MIC_no_extended.png"/>

#### Examples


```

    hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
  
```

## -see-also

<a href="/windows/desktop/tablet/customizing-the-math-input-control">Customizing the Math Input Control</a>



<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>