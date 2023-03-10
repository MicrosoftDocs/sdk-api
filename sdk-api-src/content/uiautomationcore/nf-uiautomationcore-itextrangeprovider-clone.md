---
UID: NF:uiautomationcore.ITextRangeProvider.Clone
title: ITextRangeProvider::Clone (uiautomationcore.h)
description: Returns a new ITextRangeProvider identical to the original ITextRangeProvider and inheriting all properties of the original.
helpviewer_keywords: ["Clone","Clone method [Windows Accessibility]","Clone method [Windows Accessibility]","ITextRangeProvider interface","ITextRangeProvider interface [Windows Accessibility]","Clone method","ITextRangeProvider.Clone","ITextRangeProvider::Clone","uiauto.uiauto_ITextRangeProvider_Clone","uiauto_ITextRangeProvider_Clone","uiautomationcore/ITextRangeProvider::Clone","winauto.uiauto_ITextRangeProvider_Clone"]
old-location: winauto\uiauto_ITextRangeProvider_Clone.htm
tech.root: WinAuto
ms.assetid: fe55f57b-a803-4008-adfb-b1900550d4cb
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Accessibility], Clone method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],Clone method, ITextRangeProvider.Clone, ITextRangeProvider::Clone, uiauto.uiauto_ITextRangeProvider_Clone, uiauto_ITextRangeProvider_Clone, uiautomationcore/ITextRangeProvider::Clone, winauto.uiauto_ITextRangeProvider_Clone
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
 - ITextRangeProvider::Clone
 - uiautomationcore/ITextRangeProvider::Clone
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
 - ITextRangeProvider.Clone
---

# ITextRangeProvider::Clone


## -description

Returns a new <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a> identical to the original 
        <b>ITextRangeProvider</b> and inheriting all properties of the original.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>**</b>

Receives a pointer to 
                the copy of the text range. 
                A null reference is never returned.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The new range can be manipulated independently from the original.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>