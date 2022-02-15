---
UID: NF:uiautomationcore.ILegacyIAccessibleProvider.GetIAccessible
title: ILegacyIAccessibleProvider::GetIAccessible (uiautomationcore.h)
description: Retrieves an accessible object that corresponds to a UI Automation element that supports the LegacyIAccessible control pattern.
helpviewer_keywords: ["GetIAccessible","GetIAccessible method [Windows Accessibility]","GetIAccessible method [Windows Accessibility]","ILegacyIAccessibleProvider interface","ILegacyIAccessibleProvider interface [Windows Accessibility]","GetIAccessible method","ILegacyIAccessibleProvider.GetIAccessible","ILegacyIAccessibleProvider::GetIAccessible","uiauto.uiauto_ILegacyIAccessibleProvider_GetIAccessible","uiauto_ILegacyIAccessibleProvider_GetIAccessible","uiautomationcore/ILegacyIAccessibleProvider::GetIAccessible","winauto.uiauto_ILegacyIAccessibleProvider_GetIAccessible"]
old-location: winauto\uiauto_ILegacyIAccessibleProvider_GetIAccessible.htm
tech.root: WinAuto
ms.assetid: 1d156866-d19a-4fd2-8664-d22e8b5434be
ms.date: 12/05/2018
ms.keywords: GetIAccessible, GetIAccessible method [Windows Accessibility], GetIAccessible method [Windows Accessibility],ILegacyIAccessibleProvider interface, ILegacyIAccessibleProvider interface [Windows Accessibility],GetIAccessible method, ILegacyIAccessibleProvider.GetIAccessible, ILegacyIAccessibleProvider::GetIAccessible, uiauto.uiauto_ILegacyIAccessibleProvider_GetIAccessible, uiauto_ILegacyIAccessibleProvider_GetIAccessible, uiautomationcore/ILegacyIAccessibleProvider::GetIAccessible, winauto.uiauto_ILegacyIAccessibleProvider_GetIAccessible
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
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILegacyIAccessibleProvider::GetIAccessible
 - uiautomationcore/ILegacyIAccessibleProvider::GetIAccessible
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - ILegacyIAccessibleProvider.GetIAccessible
---

# ILegacyIAccessibleProvider::GetIAccessible


## -description

Retrieves an accessible object that corresponds to a UI Automation element that supports the <a href="/windows/desktop/WinAuto/uiauto-implementinglegacyiaccessible">LegacyIAccessible</a> control pattern.

## -parameters

### -param ppAccessible [out]

Type: <b><a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>**</b>

Receives a pointer to the accessible object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ilegacyiaccessibleprovider">ILegacyIAccessibleProvider</a>