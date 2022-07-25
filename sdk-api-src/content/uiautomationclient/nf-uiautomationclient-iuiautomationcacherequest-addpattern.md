---
UID: NF:uiautomationclient.IUIAutomationCacheRequest.AddPattern
title: IUIAutomationCacheRequest::AddPattern (uiautomationclient.h)
description: Adds a control pattern to the cache request.
helpviewer_keywords: ["AddPattern","AddPattern method [Windows Accessibility]","AddPattern method [Windows Accessibility]","IUIAutomationCacheRequest interface","IUIAutomationCacheRequest interface [Windows Accessibility]","AddPattern method","IUIAutomationCacheRequest.AddPattern","IUIAutomationCacheRequest::AddPattern","uiauto.uiauto_IUIAutomationCacheRequest_AddPattern","uiauto_IUIAutomationCacheRequest_AddPattern","uiautomationclient/IUIAutomationCacheRequest::AddPattern","winauto.uiauto_IUIAutomationCacheRequest_AddPattern"]
old-location: winauto\uiauto_IUIAutomationCacheRequest_AddPattern.htm
tech.root: WinAuto
ms.assetid: f081d4da-2fba-4846-813c-33e11c09315b
ms.date: 12/05/2018
ms.keywords: AddPattern, AddPattern method [Windows Accessibility], AddPattern method [Windows Accessibility],IUIAutomationCacheRequest interface, IUIAutomationCacheRequest interface [Windows Accessibility],AddPattern method, IUIAutomationCacheRequest.AddPattern, IUIAutomationCacheRequest::AddPattern, uiauto.uiauto_IUIAutomationCacheRequest_AddPattern, uiauto_IUIAutomationCacheRequest_AddPattern, uiautomationclient/IUIAutomationCacheRequest::AddPattern, winauto.uiauto_IUIAutomationCacheRequest_AddPattern
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
 - IUIAutomationCacheRequest::AddPattern
 - uiautomationclient/IUIAutomationCacheRequest::AddPattern
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
 - IUIAutomationCacheRequest.AddPattern
---

# IUIAutomationCacheRequest::AddPattern


## -description

Adds a control pattern to the cache request.

## -parameters

### -param patternId [in]

Type: <b>PATTERNID</b>

The identifier of the control pattern to add to the cache request. For a list of control pattern IDs, see <a href="/windows/desktop/WinAuto/uiauto-controlpattern-ids">Control Pattern Identifiers</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Adding a control pattern that is already in the cache request has no effect.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>