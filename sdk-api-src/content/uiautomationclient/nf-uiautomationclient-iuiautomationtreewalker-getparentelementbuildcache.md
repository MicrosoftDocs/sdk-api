---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.GetParentElementBuildCache
title: IUIAutomationTreeWalker::GetParentElementBuildCache (uiautomationclient.h)
description: Retrieves the parent element of the specified UI Automation element, and caches properties and control patterns.
helpviewer_keywords: ["GetParentElementBuildCache","GetParentElementBuildCache method [Windows Accessibility]","GetParentElementBuildCache method [Windows Accessibility]","IUIAutomationTreeWalker interface","IUIAutomationTreeWalker interface [Windows Accessibility]","GetParentElementBuildCache method","IUIAutomationTreeWalker.GetParentElementBuildCache","IUIAutomationTreeWalker::GetParentElementBuildCache","uiauto.uiauto_IUIAutomationTreeWalker_GetParentBuildCache","uiauto_IUIAutomationTreeWalker_GetParentBuildCache","uiautomationclient/IUIAutomationTreeWalker::GetParentElementBuildCache","winauto.uiauto_IUIAutomationTreeWalker_GetParentBuildCache"]
old-location: winauto\uiauto_IUIAutomationTreeWalker_GetParentBuildCache.htm
tech.root: WinAuto
ms.assetid: 1a1d9805-bcd7-4c5d-ac61-138ac75a523e
ms.date: 12/05/2018
ms.keywords: GetParentElementBuildCache, GetParentElementBuildCache method [Windows Accessibility], GetParentElementBuildCache method [Windows Accessibility],IUIAutomationTreeWalker interface, IUIAutomationTreeWalker interface [Windows Accessibility],GetParentElementBuildCache method, IUIAutomationTreeWalker.GetParentElementBuildCache, IUIAutomationTreeWalker::GetParentElementBuildCache, uiauto.uiauto_IUIAutomationTreeWalker_GetParentBuildCache, uiauto_IUIAutomationTreeWalker_GetParentBuildCache, uiautomationclient/IUIAutomationTreeWalker::GetParentElementBuildCache, winauto.uiauto_IUIAutomationTreeWalker_GetParentBuildCache
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
 - IUIAutomationTreeWalker::GetParentElementBuildCache
 - uiautomationclient/IUIAutomationTreeWalker::GetParentElementBuildCache
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
 - IUIAutomationTreeWalker.GetParentElementBuildCache
---

# IUIAutomationTreeWalker::GetParentElementBuildCache


## -description

Retrieves the parent element of the specified UI Automation element, and caches properties and control patterns.

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element for which to retrieve the parent.

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request that specifies the properties and control patterns to cache on the returned element.

### -param parent [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the parent element, or <b>NULL</b> if there is no parent element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The structure of the Microsoft UI Automation tree changes as the visible UI elements on the desktop change. It is not guaranteed that an element returned as the  parent element will be returned as the parent on subsequent passes.