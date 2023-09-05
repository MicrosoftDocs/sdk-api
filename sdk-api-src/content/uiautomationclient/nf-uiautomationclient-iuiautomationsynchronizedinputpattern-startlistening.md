---
UID: NF:uiautomationclient.IUIAutomationSynchronizedInputPattern.StartListening
title: IUIAutomationSynchronizedInputPattern::StartListening (uiautomationclient.h)
description: Causes the Microsoft UI Automation provider to start listening for mouse or keyboard input.
helpviewer_keywords: ["IUIAutomationSynchronizedInputPattern interface [Windows Accessibility]","StartListening method","IUIAutomationSynchronizedInputPattern.StartListening","IUIAutomationSynchronizedInputPattern::StartListening","StartListening","StartListening method [Windows Accessibility]","StartListening method [Windows Accessibility]","IUIAutomationSynchronizedInputPattern interface","uiauto.uiauto_IUIAutomationSynchronizedInputPattern_StartListening","uiauto_IUIAutomationSynchronizedInputPattern_StartListening","uiautomationclient/IUIAutomationSynchronizedInputPattern::StartListening","winauto.uiauto_IUIAutomationSynchronizedInputPattern_StartListening"]
old-location: winauto\uiauto_IUIAutomationSynchronizedInputPattern_StartListening.htm
tech.root: WinAuto
ms.assetid: 2ecd413e-c1a8-404f-9a11-8c2c8428d6d7
ms.date: 12/05/2018
ms.keywords: IUIAutomationSynchronizedInputPattern interface [Windows Accessibility],StartListening method, IUIAutomationSynchronizedInputPattern.StartListening, IUIAutomationSynchronizedInputPattern::StartListening, StartListening, StartListening method [Windows Accessibility], StartListening method [Windows Accessibility],IUIAutomationSynchronizedInputPattern interface, uiauto.uiauto_IUIAutomationSynchronizedInputPattern_StartListening, uiauto_IUIAutomationSynchronizedInputPattern_StartListening, uiautomationclient/IUIAutomationSynchronizedInputPattern::StartListening, winauto.uiauto_IUIAutomationSynchronizedInputPattern_StartListening
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationSynchronizedInputPattern::StartListening
 - uiautomationclient/IUIAutomationSynchronizedInputPattern::StartListening
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationSynchronizedInputPattern.StartListening
---

# IUIAutomationSynchronizedInputPattern::StartListening


## -description

Causes the Microsoft UI Automation provider to start listening for mouse or keyboard input.

## -parameters

### -param inputType [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-synchronizedinputtype">SynchronizedInputType</a></b>

A combination of values specifying the type of input to listen for.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When matching input is found, the provider checks whether the target element matches the current element. If they match, the provider raises the <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_InputReachedTargetEventId</a> event; otherwise it raises the <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_InputReachedOtherElementEventId</a> or <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_InputDiscardedEventId</a> event.

After receiving input of the specified type, the provider stops checking for input and continues as normal.

If the provider is already listening for input, this method returns <b>E_INVALIDOPERATION</b>.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationsynchronizedinputpattern">IUIAutomationSynchronizedInputPattern</a>