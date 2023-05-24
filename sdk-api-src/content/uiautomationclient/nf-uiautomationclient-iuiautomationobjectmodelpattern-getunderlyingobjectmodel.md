---
UID: NF:uiautomationclient.IUIAutomationObjectModelPattern.GetUnderlyingObjectModel
title: IUIAutomationObjectModelPattern::GetUnderlyingObjectModel (uiautomationclient.h)
description: Retrieves an interface used to access the underlying object model of the provider. (IUIAutomationObjectModelPattern.GetUnderlyingObjectModel)
helpviewer_keywords: ["GetUnderlyingObjectModel","GetUnderlyingObjectModel method [Windows Accessibility]","GetUnderlyingObjectModel method [Windows Accessibility]","IUIAutomationObjectModelPattern interface","IUIAutomationObjectModelPattern interface [Windows Accessibility]","GetUnderlyingObjectModel method","IUIAutomationObjectModelPattern.GetUnderlyingObjectModel","IUIAutomationObjectModelPattern::GetUnderlyingObjectModel","uiautomationclient/IUIAutomationObjectModelPattern::GetUnderlyingObjectModel","winauto.uiauto_IUIAutomationObjectModelPattern_GetUnderlyingObjectModel"]
old-location: winauto\uiauto_IUIAutomationObjectModelPattern_GetUnderlyingObjectModel.htm
tech.root: WinAuto
ms.assetid: 7D1C4ABD-38FA-48C4-80ED-C0AA312D45FE
ms.date: 12/05/2018
ms.keywords: GetUnderlyingObjectModel, GetUnderlyingObjectModel method [Windows Accessibility], GetUnderlyingObjectModel method [Windows Accessibility],IUIAutomationObjectModelPattern interface, IUIAutomationObjectModelPattern interface [Windows Accessibility],GetUnderlyingObjectModel method, IUIAutomationObjectModelPattern.GetUnderlyingObjectModel, IUIAutomationObjectModelPattern::GetUnderlyingObjectModel, uiautomationclient/IUIAutomationObjectModelPattern::GetUnderlyingObjectModel, winauto.uiauto_IUIAutomationObjectModelPattern_GetUnderlyingObjectModel
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IUIAutomationObjectModelPattern::GetUnderlyingObjectModel
 - uiautomationclient/IUIAutomationObjectModelPattern::GetUnderlyingObjectModel
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
 - IUIAutomationObjectModelPattern.GetUnderlyingObjectModel
---

# IUIAutomationObjectModelPattern::GetUnderlyingObjectModel


## -description

Retrieves an interface used to access the underlying object model of the provider.

## -parameters

### -param retVal [out, retval]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives an interface for accessing the underlying object model.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Client applications can use the object model to directly access the content of the control or application.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationobjectmodelpattern">IUIAutomationObjectModelPattern</a>
