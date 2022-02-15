---
UID: NF:uiautomationclient.IUIAutomationCacheRequest.AddProperty
title: IUIAutomationCacheRequest::AddProperty (uiautomationclient.h)
description: Adds a property to the cache request.
helpviewer_keywords: ["AddProperty","AddProperty method [Windows Accessibility]","AddProperty method [Windows Accessibility]","IUIAutomationCacheRequest interface","IUIAutomationCacheRequest interface [Windows Accessibility]","AddProperty method","IUIAutomationCacheRequest.AddProperty","IUIAutomationCacheRequest::AddProperty","uiauto.uiauto_IUIAutomationCacheRequest_AddProperty","uiauto_IUIAutomationCacheRequest_AddProperty","uiautomationclient/IUIAutomationCacheRequest::AddProperty","winauto.uiauto_IUIAutomationCacheRequest_AddProperty"]
old-location: winauto\uiauto_IUIAutomationCacheRequest_AddProperty.htm
tech.root: WinAuto
ms.assetid: 61e56133-fb9e-4556-a9be-f7270b1d2bfb
ms.date: 12/05/2018
ms.keywords: AddProperty, AddProperty method [Windows Accessibility], AddProperty method [Windows Accessibility],IUIAutomationCacheRequest interface, IUIAutomationCacheRequest interface [Windows Accessibility],AddProperty method, IUIAutomationCacheRequest.AddProperty, IUIAutomationCacheRequest::AddProperty, uiauto.uiauto_IUIAutomationCacheRequest_AddProperty, uiauto_IUIAutomationCacheRequest_AddProperty, uiautomationclient/IUIAutomationCacheRequest::AddProperty, winauto.uiauto_IUIAutomationCacheRequest_AddProperty
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
 - IUIAutomationCacheRequest::AddProperty
 - uiautomationclient/IUIAutomationCacheRequest::AddProperty
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
 - IUIAutomationCacheRequest.AddProperty
---

# IUIAutomationCacheRequest::AddProperty


## -description

Adds a property to the cache request.

## -parameters

### -param propertyId [in]

Type: <b>PROPERTYID</b>

A property identifier.  For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>