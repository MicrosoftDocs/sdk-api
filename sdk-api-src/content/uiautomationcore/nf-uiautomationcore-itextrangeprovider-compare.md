---
UID: NF:uiautomationcore.ITextRangeProvider.Compare
title: ITextRangeProvider::Compare (uiautomationcore.h)
author: windows-sdk-content
description: Retrieves a value that specifies whether this text range has the same endpoints as another text range.
old-location: winauto\uiauto_ITextRangeProvider_Compare.htm
tech.root: WinAuto
ms.assetid: 6ccdeeee-4c9b-439b-abb8-1fc71f3d209c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Compare, Compare method [Windows Accessibility], Compare method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],Compare method, ITextRangeProvider.Compare, ITextRangeProvider::Compare, uiauto.uiauto_ITextRangeProvider_Compare, uiauto_ITextRangeProvider_Compare, uiautomationcore/ITextRangeProvider::Compare, winauto.uiauto_ITextRangeProvider_Compare
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextRangeProvider.Compare
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextRangeProvider::Compare


## -description


Retrieves a value that specifies whether this text range has the same endpoints as another text range.


## -parameters




### -param range [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>*</b>

The text range to compare with this one.


### -param pRetVal [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Receives <b>TRUE</b> if the text ranges have the same endpoints, or <b>FALSE</b> if they do not.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method compares the endpoints of the two text ranges, not the text in the ranges. The ranges are identical if they share the same endpoints. If two text ranges have different endpoints, they are not identical even if the text in both ranges is exactly the same. 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

