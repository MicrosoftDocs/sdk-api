---
UID: NF:uiautomationcore.IAccessibleEx.GetObjectForChild
title: IAccessibleEx::GetObjectForChild (uiautomationcore.h)
description: Retrieves an IAccessibleEx interface representing the specified child of this element.
helpviewer_keywords: ["GetObjectForChild","GetObjectForChild method [Windows Accessibility]","GetObjectForChild method [Windows Accessibility]","IAccessibleEx interface","IAccessibleEx interface [Windows Accessibility]","GetObjectForChild method","IAccessibleEx.GetObjectForChild","IAccessibleEx::GetObjectForChild","uiauto.uiauto_IAccessibleEx_GetObjectForChild","uiauto_IAccessibleEx_GetObjectForChild","uiautomationcore/IAccessibleEx::GetObjectForChild","winauto.uiauto_IAccessibleEx_GetObjectForChild"]
old-location: winauto\uiauto_IAccessibleEx_GetObjectForChild.htm
tech.root: WinAuto
ms.assetid: fbb279cc-2224-437e-875b-d08df175edf1
ms.date: 12/05/2018
ms.keywords: GetObjectForChild, GetObjectForChild method [Windows Accessibility], GetObjectForChild method [Windows Accessibility],IAccessibleEx interface, IAccessibleEx interface [Windows Accessibility],GetObjectForChild method, IAccessibleEx.GetObjectForChild, IAccessibleEx::GetObjectForChild, uiauto.uiauto_IAccessibleEx_GetObjectForChild, uiauto_IAccessibleEx_GetObjectForChild, uiautomationcore/IAccessibleEx::GetObjectForChild, winauto.uiauto_IAccessibleEx_GetObjectForChild
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAccessibleEx::GetObjectForChild
 - uiautomationcore/IAccessibleEx::GetObjectForChild
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
 - IAccessibleEx.GetObjectForChild
---

# IAccessibleEx::GetObjectForChild


## -description

Retrieves an <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a> interface representing the specified child of this element.

## -parameters

### -param idChild [in]

Type: <b>long</b>

The identifier of the child element.

### -param pRetVal [out]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a>**</b>

Receives a pointer to the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a> interface.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<i>pRetVal</i> returns <b>NULL</b> if this implementation does not use child IDs, or cannot provide an <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a> interface for the specified child, or itself represents a child element.

<i>idChild</i> must represent an actual MSAA child element, not an object that has its own <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a>