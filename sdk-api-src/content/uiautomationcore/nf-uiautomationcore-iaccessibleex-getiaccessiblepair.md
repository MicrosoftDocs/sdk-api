---
UID: NF:uiautomationcore.IAccessibleEx.GetIAccessiblePair
title: IAccessibleEx::GetIAccessiblePair (uiautomationcore.h)
description: Retrieves the IAccessible interface and child ID for this item.
helpviewer_keywords: ["GetIAccessiblePair","GetIAccessiblePair method [Windows Accessibility]","GetIAccessiblePair method [Windows Accessibility]","IAccessibleEx interface","IAccessibleEx interface [Windows Accessibility]","GetIAccessiblePair method","IAccessibleEx.GetIAccessiblePair","IAccessibleEx::GetIAccessiblePair","uiauto.uiauto_IAccessibleEx_GetIAccessiblePair","uiauto_IAccessibleEx_GetIAccessiblePair","uiautomationcore/IAccessibleEx::GetIAccessiblePair","winauto.uiauto_IAccessibleEx_GetIAccessiblePair"]
old-location: winauto\uiauto_IAccessibleEx_GetIAccessiblePair.htm
tech.root: WinAuto
ms.assetid: 282de8b1-67ce-42e3-9f17-dbd29374d910
ms.date: 12/05/2018
ms.keywords: GetIAccessiblePair, GetIAccessiblePair method [Windows Accessibility], GetIAccessiblePair method [Windows Accessibility],IAccessibleEx interface, IAccessibleEx interface [Windows Accessibility],GetIAccessiblePair method, IAccessibleEx.GetIAccessiblePair, IAccessibleEx::GetIAccessiblePair, uiauto.uiauto_IAccessibleEx_GetIAccessiblePair, uiauto_IAccessibleEx_GetIAccessiblePair, uiautomationcore/IAccessibleEx::GetIAccessiblePair, winauto.uiauto_IAccessibleEx_GetIAccessiblePair
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
 - IAccessibleEx::GetIAccessiblePair
 - uiautomationcore/IAccessibleEx::GetIAccessiblePair
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
 - IAccessibleEx.GetIAccessiblePair
---

# IAccessibleEx::GetIAccessiblePair


## -description

Retrieves the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface and child ID for this item.

## -parameters

### -param ppAcc [out]

Type: <b><a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>**</b>

Receives a pointer to the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface for this object, or the parent object if this is a child element.

### -param pidChild [out]

Type: <b>long*</b>

Receives the child ID, or CHILDID_SELF if this is not a child element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a>