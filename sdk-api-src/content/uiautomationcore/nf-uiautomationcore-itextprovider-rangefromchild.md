---
UID: NF:uiautomationcore.ITextProvider.RangeFromChild
title: ITextProvider::RangeFromChild (uiautomationcore.h)
author: windows-sdk-content
description: Retrieves a text range enclosing a child element such as an image, hyperlink, or other embedded object.
old-location: winauto\uiauto_ITextProvider_RangeFromChild.htm
tech.root: WinAuto
ms.assetid: b55ae687-44e1-499f-8341-0bbf960529fd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextProvider interface [Windows Accessibility],RangeFromChild method, ITextProvider.RangeFromChild, ITextProvider::RangeFromChild, RangeFromChild, RangeFromChild method [Windows Accessibility], RangeFromChild method [Windows Accessibility],ITextProvider interface, uiauto.uiauto_ITextProvider_RangeFromChild, uiauto_ITextProvider_RangeFromChild, uiautomationcore/ITextProvider::RangeFromChild, winauto.uiauto_ITextProvider_RangeFromChild
ms.topic: method
f1_keywords: 
 - "uiautomationcore/ITextProvider.RangeFromChild"
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
 - ITextProvider.RangeFromChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextProvider::RangeFromChild


## -description


Retrieves a text range enclosing a child element such as an image, hyperlink, or other embedded object. 
        


## -parameters




### -param childElement [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

The address of the UI Automation provider interface for the enclosed UI Automation object.


### -param pRetVal [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>**</b>

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">text range</a> 
				that spans the child element. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A provider should check that the passed element is a child of the text container.

If there is no text in the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">text range</a> where the child element exists, a degenerate (empty) range is returned.

The <i>childElement</i> parameter is either a child of the UI Automation element associated with a TextPattern or from the array of children of an <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>.
			




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

