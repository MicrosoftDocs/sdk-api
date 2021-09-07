---
UID: NF:uiautomationcore.ITextProvider.RangeFromPoint
title: ITextProvider::RangeFromPoint (uiautomationcore.h)
description: Returns the degenerate (empty) text range nearest to the specified screen coordinates.
helpviewer_keywords: ["ITextProvider interface [Windows Accessibility]","RangeFromPoint method","ITextProvider.RangeFromPoint","ITextProvider::RangeFromPoint","RangeFromPoint","RangeFromPoint method [Windows Accessibility]","RangeFromPoint method [Windows Accessibility]","ITextProvider interface","uiauto.uiauto_ITextProvider_RangeFromPoint","uiauto_ITextProvider_RangeFromPoint","uiautomationcore/ITextProvider::RangeFromPoint","winauto.uiauto_ITextProvider_RangeFromPoint"]
old-location: winauto\uiauto_ITextProvider_RangeFromPoint.htm
tech.root: WinAuto
ms.assetid: c19c6a4a-b783-47c2-8dfd-1ffe947278f0
ms.date: 12/05/2018
ms.keywords: ITextProvider interface [Windows Accessibility],RangeFromPoint method, ITextProvider.RangeFromPoint, ITextProvider::RangeFromPoint, RangeFromPoint, RangeFromPoint method [Windows Accessibility], RangeFromPoint method [Windows Accessibility],ITextProvider interface, uiauto.uiauto_ITextProvider_RangeFromPoint, uiauto_ITextProvider_RangeFromPoint, uiautomationcore/ITextProvider::RangeFromPoint, winauto.uiauto_ITextProvider_RangeFromPoint
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - ITextProvider::RangeFromPoint
 - uiautomationcore/ITextProvider::RangeFromPoint
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
 - ITextProvider.RangeFromPoint
---

# ITextProvider::RangeFromPoint


## -description

Returns the degenerate (empty) text range nearest to the specified screen coordinates.

## -parameters

### -param point [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiapoint">UiaPoint</a></b>

The location in screen coordinates.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>**</b>

Receives a pointer to the degenerate (empty) text range 
				nearest the specified location. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A text range that encloses a child object is returned if the screen coordinates are 
            within the coordinates of an image, hyperlink, or other embedded object. 
            

Because hidden text is not ignored by <b>ITextProvider::RangeFromPoint</b>, a degenerate range from the visible text 
			closest to the given point is returned.

The property never returns <b>NULL</b>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>