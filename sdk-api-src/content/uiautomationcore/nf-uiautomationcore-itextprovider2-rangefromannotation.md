---
UID: NF:uiautomationcore.ITextProvider2.RangeFromAnnotation
title: ITextProvider2::RangeFromAnnotation (uiautomationcore.h)
description: Exposes a text range that contains the text that is the target of the annotation associated with the specified annotation element.
helpviewer_keywords: ["ITextProvider2 interface [Windows Accessibility]","RangeFromAnnotation method","ITextProvider2.RangeFromAnnotation","ITextProvider2::RangeFromAnnotation","RangeFromAnnotation","RangeFromAnnotation method [Windows Accessibility]","RangeFromAnnotation method [Windows Accessibility]","ITextProvider2 interface","uiautomationcore/ITextProvider2::RangeFromAnnotation","winauto.uiauto_itextprovider2_rangefromannotation"]
old-location: winauto\uiauto_itextprovider2_rangefromannotation.htm
tech.root: WinAuto
ms.assetid: 908DEDED-1AF9-4DFF-AC1D-F06818B06925
ms.date: 12/05/2018
ms.keywords: ITextProvider2 interface [Windows Accessibility],RangeFromAnnotation method, ITextProvider2.RangeFromAnnotation, ITextProvider2::RangeFromAnnotation, RangeFromAnnotation, RangeFromAnnotation method [Windows Accessibility], RangeFromAnnotation method [Windows Accessibility],ITextProvider2 interface, uiautomationcore/ITextProvider2::RangeFromAnnotation, winauto.uiauto_itextprovider2_rangefromannotation
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - ITextProvider2::RangeFromAnnotation
 - uiautomationcore/ITextProvider2::RangeFromAnnotation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextProvider2.RangeFromAnnotation
---

# ITextProvider2::RangeFromAnnotation


## -description

Exposes a text range that contains the text that is the target of the annotation associated with the specified annotation element.

## -parameters

### -param annotationElement [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

The provider for an element that implements the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider">IAnnotationProvider</a> interface. The annotation element is a sibling of the element that implements the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2">ITextProvider2</a> interface for the document.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>**</b>

Receives a text range that contains the annotation target text.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-supportdocumentcontroltype">Document Control Type</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2">ITextProvider2</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>