---
UID: NF:uiautomationclient.IUIAutomationCacheRequest.Clone
title: IUIAutomationCacheRequest::Clone
author: windows-sdk-content
description: Creates a copy of the cache request.
old-location: winauto\uiauto_IUIAutomationCacheRequest_Clone.htm
tech.root: WinAuto
ms.assetid: e7ba5cb0-a4a5-4556-ba28-899e9635af5d
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: Clone, Clone method [Windows Accessibility], Clone method [Windows Accessibility],IUIAutomationCacheRequest interface, IUIAutomationCacheRequest interface [Windows Accessibility],Clone method, IUIAutomationCacheRequest.Clone, IUIAutomationCacheRequest::Clone, uiauto.uiauto_IUIAutomationCacheRequest_Clone, uiauto_IUIAutomationCacheRequest_Clone, uiautomationclient/IUIAutomationCacheRequest::Clone, winauto.uiauto_IUIAutomationCacheRequest_Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationCacheRequest.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationCacheRequest::Clone


## -description


Creates a copy of the cache request.


## -parameters




### -param clonedRequest [out, retval]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>**</b>

Receives a pointer to the copy of the cache request.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



