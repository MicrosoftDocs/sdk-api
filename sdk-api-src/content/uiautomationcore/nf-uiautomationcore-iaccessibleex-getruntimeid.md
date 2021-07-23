---
UID: NF:uiautomationcore.IAccessibleEx.GetRuntimeId
title: IAccessibleEx::GetRuntimeId (uiautomationcore.h)
description: Retrieves the runtime identifier of this element.
helpviewer_keywords: ["GetRuntimeId","GetRuntimeId method [Windows Accessibility]","GetRuntimeId method [Windows Accessibility]","IAccessibleEx interface","IAccessibleEx interface [Windows Accessibility]","GetRuntimeId method","IAccessibleEx.GetRuntimeId","IAccessibleEx::GetRuntimeId","uiauto.uiauto_IAccessibleEx_GetRuntimeId","uiauto_IAccessibleEx_GetRuntimeId","uiautomationcore/IAccessibleEx::GetRuntimeId","winauto.uiauto_IAccessibleEx_GetRuntimeId"]
old-location: winauto\uiauto_IAccessibleEx_GetRuntimeId.htm
tech.root: WinAuto
ms.assetid: 00aeac66-398a-4c80-85e2-32bff0ae100f
ms.date: 12/05/2018
ms.keywords: GetRuntimeId, GetRuntimeId method [Windows Accessibility], GetRuntimeId method [Windows Accessibility],IAccessibleEx interface, IAccessibleEx interface [Windows Accessibility],GetRuntimeId method, IAccessibleEx.GetRuntimeId, IAccessibleEx::GetRuntimeId, uiauto.uiauto_IAccessibleEx_GetRuntimeId, uiauto_IAccessibleEx_GetRuntimeId, uiautomationcore/IAccessibleEx::GetRuntimeId, winauto.uiauto_IAccessibleEx_GetRuntimeId
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
 - IAccessibleEx::GetRuntimeId
 - uiautomationcore/IAccessibleEx::GetRuntimeId
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
 - IAccessibleEx.GetRuntimeId
---

# IAccessibleEx::GetRuntimeId


## -description

Retrieves the runtime identifier of this element.

## -parameters

### -param pRetVal [out]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to the runtime identifier.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The runtime identifier is a provider-defined array of integers, the first item of which must be <b>UiaAppendRuntimeId</b>. The runtime identifier must be unique within the parent window.

The MSAA-to-UIA Proxy uses the runtime identifier (together with the window handle) to determine if two interface instances refer to the same underlying element. If <b>IAccessibleEx::GetRuntimeId</b> is not implemented, the proxy performs field-by-field comparisons on the two <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> objects to determine if they are equivalent, which is less efficient.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a>



<b>Reference</b>