---
UID: NN:uiautomationclient.IUIAutomationCacheRequest
title: IUIAutomationCacheRequest (uiautomationclient.h)
description: Exposes properties and methods of a cache request. Client applications use this interface to specify the properties and control patterns to be cached when a Microsoft UI Automation element is obtained.
helpviewer_keywords: ["IUIAutomationCacheRequest","IUIAutomationCacheRequest interface [Windows Accessibility]","IUIAutomationCacheRequest interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationCacheRequest","uiauto_IUIAutomationCacheRequest","uiautomationclient/IUIAutomationCacheRequest","winauto.uiauto_IUIAutomationCacheRequest"]
old-location: winauto\uiauto_IUIAutomationCacheRequest.htm
tech.root: WinAuto
ms.assetid: 8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41
ms.date: 12/05/2018
ms.keywords: IUIAutomationCacheRequest, IUIAutomationCacheRequest interface [Windows Accessibility], IUIAutomationCacheRequest interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationCacheRequest, uiauto_IUIAutomationCacheRequest, uiautomationclient/IUIAutomationCacheRequest, winauto.uiauto_IUIAutomationCacheRequest
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
 - IUIAutomationCacheRequest
 - uiautomationclient/IUIAutomationCacheRequest
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
 - IUIAutomationCacheRequest
---

# IUIAutomationCacheRequest interface


## -description

Exposes properties and methods of a cache request. Client applications use this interface to specify the properties and control patterns to be cached when a Microsoft UI Automation element is obtained.

## -inheritance

The <b>IUIAutomationCacheRequest</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationCacheRequest</b> also has these types of members:

## -remarks

Retrieving properties and control patterns through UI Automation requires cross-process calls that can slow down performance. By caching values of proprieties and control patterns in a batch operation, you can enhance the performance of your application.

Create a new cache request by calling <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createcacherequest">CreateCacheRequest</a>, and configure the request by calling methods of <b>IUIAutomationCacheRequest</b>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>
