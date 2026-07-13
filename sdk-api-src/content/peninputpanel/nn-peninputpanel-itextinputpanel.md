---
UID: NN:peninputpanel.ITextInputPanel
title: ITextInputPanel (peninputpanel.h)
description: Provides control of appearance and behavior of the Tablet PC Input Panel.
helpviewer_keywords: ["1e719900-db58-430d-9059-efb3f884f6f0","ITextInputPanel","ITextInputPanel interface [Tablet PC]","ITextInputPanel interface [Tablet PC]","described","peninputpanel/ITextInputPanel","tablet.itextinputpanel"]
old-location: tablet\itextinputpanel.htm
tech.root: tablet
ms.assetid: 1e719900-db58-430d-9059-efb3f884f6f0
ms.date: 12/05/2018
ms.keywords: 1e719900-db58-430d-9059-efb3f884f6f0, ITextInputPanel, ITextInputPanel interface [Tablet PC], ITextInputPanel interface [Tablet PC],described, peninputpanel/ITextInputPanel, tablet.itextinputpanel
req.header: peninputpanel.h
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
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextInputPanel
 - peninputpanel/ITextInputPanel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITextInputPanel
---

# ITextInputPanel interface


## -description

**ITextInputPanel** is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use [IInputPanelConfiguration interface](../inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration.md).

Provides control of appearance and behavior of the Tablet PC Input Panel.

## -inheritance

The <b>ITextInputPanel</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextInputPanel</b> also has these types of members:

## -remarks

<b>ITextInputPanel Interface</b> gives application developers more control and information about Input Panel's state than <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel Class</a>. <b>ITextInputPanel Interface</b> replaces the <b>PenInputPanel Class</b> as the preferred mechanism for programmatically interacting with the Input Panel.

<b>ITextInputPanel Interface</b> provides:

<ul>
<li>A complete control over the positioning of the in-place Input Panel when the application has focus.</li>
<li>An access to the ink objects from the Input Panel text insertion in addition to the recognized text.</li>
<li>A set of properties that correspond exactly to Input Panel's capabilities giving both the ability to know Input Panel's current state and to customize Input Panel's configuration.</li>
</ul>
The <b>ITextInputPanel Interface</b> continues to provide nearly all of the programmatic capabilities of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel Class</a> thus superseding the <b>PenInputPanel Class</b>.

This element is declared in Peninputpanel.h.
