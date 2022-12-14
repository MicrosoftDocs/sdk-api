---
UID: NF:uiautomationcore.IObjectModelProvider.GetUnderlyingObjectModel
title: IObjectModelProvider::GetUnderlyingObjectModel (uiautomationcore.h)
description: Retrieves an interface used to access the underlying object model of the provider. (IObjectModelProvider.GetUnderlyingObjectModel)
helpviewer_keywords: ["GetUnderlyingObjectModel","GetUnderlyingObjectModel method [Windows Accessibility]","GetUnderlyingObjectModel method [Windows Accessibility]","IObjectModelProvider interface","IObjectModelProvider interface [Windows Accessibility]","GetUnderlyingObjectModel method","IObjectModelProvider.GetUnderlyingObjectModel","IObjectModelProvider::GetUnderlyingObjectModel","uiautomationcore/IObjectModelProvider::GetUnderlyingObjectModel","winauto.uiauto_IObjectModelProvider_GetUnderlyingObjectModel"]
old-location: winauto\uiauto_IObjectModelProvider_GetUnderlyingObjectModel.htm
tech.root: WinAuto
ms.assetid: 305758A1-D584-45A3-B118-B46B3731820D
ms.date: 12/05/2018
ms.keywords: GetUnderlyingObjectModel, GetUnderlyingObjectModel method [Windows Accessibility], GetUnderlyingObjectModel method [Windows Accessibility],IObjectModelProvider interface, IObjectModelProvider interface [Windows Accessibility],GetUnderlyingObjectModel method, IObjectModelProvider.GetUnderlyingObjectModel, IObjectModelProvider::GetUnderlyingObjectModel, uiautomationcore/IObjectModelProvider::GetUnderlyingObjectModel, winauto.uiauto_IObjectModelProvider_GetUnderlyingObjectModel
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
 - IObjectModelProvider::GetUnderlyingObjectModel
 - uiautomationcore/IObjectModelProvider::GetUnderlyingObjectModel
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
 - IObjectModelProvider.GetUnderlyingObjectModel
---

# IObjectModelProvider::GetUnderlyingObjectModel


## -description

Retrieves an interface used to access the underlying object model of the provider.

## -parameters

### -param ppUnknown [out, retval]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives an interface for accessing the underlying object model.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Client applications can use the object model to directly access the content of the control or application.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider">IObjectModelProvider</a>
