---
UID: NF:uiautomationclient.IUIAutomation.CreateCacheRequest
title: IUIAutomation::CreateCacheRequest (uiautomationclient.h)
description: Creates a cache request.
helpviewer_keywords: ["CreateCacheRequest","CreateCacheRequest method [Windows Accessibility]","CreateCacheRequest method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CreateCacheRequest method","IUIAutomation.CreateCacheRequest","IUIAutomation::CreateCacheRequest","uiauto.uiauto_IUIAutomation_CreateCacheRequest","uiauto_IUIAutomation_CreateCacheRequest","uiautomationclient/IUIAutomation::CreateCacheRequest","winauto.uiauto_IUIAutomation_CreateCacheRequest"]
old-location: winauto\uiauto_IUIAutomation_CreateCacheRequest.htm
tech.root: WinAuto
ms.assetid: e61aecac-8c08-4f83-b3e6-f4baedcb16c6
ms.date: 12/05/2018
ms.keywords: CreateCacheRequest, CreateCacheRequest method [Windows Accessibility], CreateCacheRequest method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateCacheRequest method, IUIAutomation.CreateCacheRequest, IUIAutomation::CreateCacheRequest, uiauto.uiauto_IUIAutomation_CreateCacheRequest, uiauto_IUIAutomation_CreateCacheRequest, uiautomationclient/IUIAutomation::CreateCacheRequest, winauto.uiauto_IUIAutomation_CreateCacheRequest
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
 - IUIAutomation::CreateCacheRequest
 - uiautomationclient/IUIAutomation::CreateCacheRequest
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
 - IUIAutomation.CreateCacheRequest
---

# IUIAutomation::CreateCacheRequest


## -description

Creates a cache request.

## -parameters

### -param cacheRequest [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>**</b>

The address of a variable that receives a pointer to an <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a> interface.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After obtaining the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a> interface, use its methods to specify properties and control patterns to be cached when a UI Automation element is obtained.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-cachingforclients">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtreewalker">IUIAutomationTreeWalker</a>



<b>Reference</b>