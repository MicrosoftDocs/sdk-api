---
UID: NF:uiautomationclient.IUIAutomationCacheRequest.Clone
title: IUIAutomationCacheRequest::Clone (uiautomationclient.h)
description: Creates a copy of the cache request.
helpviewer_keywords: ["Clone","Clone method [Windows Accessibility]","Clone method [Windows Accessibility]","IUIAutomationCacheRequest interface","IUIAutomationCacheRequest interface [Windows Accessibility]","Clone method","IUIAutomationCacheRequest.Clone","IUIAutomationCacheRequest::Clone","uiauto.uiauto_IUIAutomationCacheRequest_Clone","uiauto_IUIAutomationCacheRequest_Clone","uiautomationclient/IUIAutomationCacheRequest::Clone","winauto.uiauto_IUIAutomationCacheRequest_Clone"]
old-location: winauto\uiauto_IUIAutomationCacheRequest_Clone.htm
tech.root: WinAuto
ms.assetid: e7ba5cb0-a4a5-4556-ba28-899e9635af5d
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Accessibility], Clone method [Windows Accessibility],IUIAutomationCacheRequest interface, IUIAutomationCacheRequest interface [Windows Accessibility],Clone method, IUIAutomationCacheRequest.Clone, IUIAutomationCacheRequest::Clone, uiauto.uiauto_IUIAutomationCacheRequest_Clone, uiauto_IUIAutomationCacheRequest_Clone, uiautomationclient/IUIAutomationCacheRequest::Clone, winauto.uiauto_IUIAutomationCacheRequest_Clone
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
 - IUIAutomationCacheRequest::Clone
 - uiautomationclient/IUIAutomationCacheRequest::Clone
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
 - IUIAutomationCacheRequest.Clone
---

# IUIAutomationCacheRequest::Clone


## -description

Creates a copy of the cache request.

## -parameters

### -param clonedRequest [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>**</b>

Receives a pointer to the copy of the cache request.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.