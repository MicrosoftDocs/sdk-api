---
UID: NF:uiautomationcore.ISynchronizedInputProvider.StartListening
title: ISynchronizedInputProvider::StartListening (uiautomationcore.h)
description: Starts listening for input of the specified type.
helpviewer_keywords: ["ISynchronizedInputProvider interface [Windows Accessibility]","StartListening method","ISynchronizedInputProvider.StartListening","ISynchronizedInputProvider::StartListening","StartListening","StartListening method [Windows Accessibility]","StartListening method [Windows Accessibility]","ISynchronizedInputProvider interface","uiauto.uiauto_ISynchronizedInputProvider_StartListening","uiauto_ISynchronizedInputProvider_StartListening","uiautomationcore/ISynchronizedInputProvider::StartListening","winauto.uiauto_ISynchronizedInputProvider_StartListening"]
old-location: winauto\uiauto_ISynchronizedInputProvider_StartListening.htm
tech.root: WinAuto
ms.assetid: ad9e6ca3-b38c-41f8-9c61-ce51786672eb
ms.date: 12/05/2018
ms.keywords: ISynchronizedInputProvider interface [Windows Accessibility],StartListening method, ISynchronizedInputProvider.StartListening, ISynchronizedInputProvider::StartListening, StartListening, StartListening method [Windows Accessibility], StartListening method [Windows Accessibility],ISynchronizedInputProvider interface, uiauto.uiauto_ISynchronizedInputProvider_StartListening, uiauto_ISynchronizedInputProvider_StartListening, uiautomationcore/ISynchronizedInputProvider::StartListening, winauto.uiauto_ISynchronizedInputProvider_StartListening
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - ISynchronizedInputProvider::StartListening
 - uiautomationcore/ISynchronizedInputProvider::StartListening
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
 - ISynchronizedInputProvider.StartListening
---

# ISynchronizedInputProvider::StartListening


## -description

Starts listening for input of the specified type.

## -parameters

### -param inputType [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-synchronizedinputtype">SynchronizedInputType</a></b>

The type of input that is requested to be synchronized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When it finds matching input, the provider checks if the target UI Automation element matches the current element. If they match, the provider raises the <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_InputReachedTargetEventId</a> event; otherwise, it raises the <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_InputReachedOtherElementEventId</a>  or <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_InputDiscardedEventId</a> event. The UI Automation provider must discard the input if it is for an element other than this one.

This is a one-shot method; after receiving input, the provider stops listening and continues normally.

This method returns E_INVALIDOPERATION if the provider is already listening for input.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-isynchronizedinputprovider">ISynchronizedInputProvider</a>