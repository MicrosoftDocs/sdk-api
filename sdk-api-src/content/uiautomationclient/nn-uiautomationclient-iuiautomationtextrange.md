---
UID: NN:uiautomationclient.IUIAutomationTextRange
title: IUIAutomationTextRange (uiautomationclient.h)
description: Provides access to a span of continuous text in a container that supports the IUIAutomationTextPattern interface. Client applications can use the IUIAutomationTextRange interface to select, compare, and retrieve embedded objects from the text span.
helpviewer_keywords: ["IUIAutomationTextRange","IUIAutomationTextRange interface [Windows Accessibility]","IUIAutomationTextRange interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationTextRange","uiauto_IUIAutomationTextRange","uiautomationclient/IUIAutomationTextRange","winauto.uiauto_IUIAutomationTextRange"]
old-location: winauto\uiauto_IUIAutomationTextRange.htm
tech.root: WinAuto
ms.assetid: 1037919d-c8df-4d46-b3ce-62ee23c92145
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextRange, IUIAutomationTextRange interface [Windows Accessibility], IUIAutomationTextRange interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTextRange, uiauto_IUIAutomationTextRange, uiautomationclient/IUIAutomationTextRange, winauto.uiauto_IUIAutomationTextRange
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationTextRange
 - uiautomationclient/IUIAutomationTextRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationTextRange
---

# IUIAutomationTextRange interface


## -description

Provides access to  a span of continuous text in a container that supports the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a> interface. Client applications can use the <b>IUIAutomationTextRange</b> interface to select, compare, and retrieve embedded objects from the text span. The interface uses two endpoints to delimit where the text span starts and ends. Disjoint spans of text are represented by an <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrangearray">IUIAutomationTextRangeArray</a> interface.

## -inheritance

The <b>IUIAutomationTextRange</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationTextRange</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>



<a href="/windows/desktop/WinAuto/uiauto-usingtextrangeobjects">Using Text Ranges</a>
