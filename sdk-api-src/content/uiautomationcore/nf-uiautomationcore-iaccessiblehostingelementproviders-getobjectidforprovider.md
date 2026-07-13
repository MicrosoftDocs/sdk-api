---
UID: NF:uiautomationcore.IAccessibleHostingElementProviders.GetObjectIdForProvider
title: IAccessibleHostingElementProviders::GetObjectIdForProvider (uiautomationcore.h)
description: Retrieves the object ID associated with a contained windowless Microsoft ActiveX control that implements Microsoft UI Automation.
helpviewer_keywords: ["GetObjectIdForProvider","GetObjectIdForProvider method [Windows Accessibility]","GetObjectIdForProvider method [Windows Accessibility]","IAccessibleHostingElementProviders interface","IAccessibleHostingElementProviders interface [Windows Accessibility]","GetObjectIdForProvider method","IAccessibleHostingElementProviders.GetObjectIdForProvider","IAccessibleHostingElementProviders::GetObjectIdForProvider","uiautomationcore/IAccessibleHostingElementProviders::GetObjectIdForProvider","winauto.uiauto_IAccessibleHostingElementProviders_GetObjectIdForProvider"]
old-location: winauto\uiauto_IAccessibleHostingElementProviders_GetObjectIdForProvider.htm
tech.root: WinAuto
ms.assetid: 847F285F-F31D-486C-BBC7-DEED69505306
ms.date: 12/05/2018
ms.keywords: GetObjectIdForProvider, GetObjectIdForProvider method [Windows Accessibility], GetObjectIdForProvider method [Windows Accessibility],IAccessibleHostingElementProviders interface, IAccessibleHostingElementProviders interface [Windows Accessibility],GetObjectIdForProvider method, IAccessibleHostingElementProviders.GetObjectIdForProvider, IAccessibleHostingElementProviders::GetObjectIdForProvider, uiautomationcore/IAccessibleHostingElementProviders::GetObjectIdForProvider, winauto.uiauto_IAccessibleHostingElementProviders_GetObjectIdForProvider
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IAccessibleHostingElementProviders::GetObjectIdForProvider
 - uiautomationcore/IAccessibleHostingElementProviders::GetObjectIdForProvider
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
 - IAccessibleHostingElementProviders.GetObjectIdForProvider
---

# IAccessibleHostingElementProviders::GetObjectIdForProvider


## -description

Retrieves the object ID associated with a contained windowless Microsoft ActiveX control that implements Microsoft UI Automation.

## -parameters

### -param pProvider [in, optional]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

The provider for the windowless ActiveX control.

### -param pidObject [out]

Type: <b>long*</b>

The object ID of the contained windowless ActiveX control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessiblehostingelementproviders">IAccessibleHostingElementProviders</a>