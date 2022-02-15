---
UID: NF:uiautomationcore.ILegacyIAccessibleProvider.SetValue
title: ILegacyIAccessibleProvider::SetValue (uiautomationcore.h)
description: Sets the string value of the control.
helpviewer_keywords: ["ILegacyIAccessibleProvider interface [Windows Accessibility]","SetValue method","ILegacyIAccessibleProvider.SetValue","ILegacyIAccessibleProvider::SetValue","SetValue","SetValue method [Windows Accessibility]","SetValue method [Windows Accessibility]","ILegacyIAccessibleProvider interface","uiauto.uiauto_ILegacyIAccessibleProvider_SetValue","uiauto_ILegacyIAccessibleProvider_SetValue","uiautomationcore/ILegacyIAccessibleProvider::SetValue","winauto.uiauto_ILegacyIAccessibleProvider_SetValue"]
old-location: winauto\uiauto_ILegacyIAccessibleProvider_SetValue.htm
tech.root: WinAuto
ms.assetid: ca0901af-8d79-4aed-876f-0d719657ef12
ms.date: 12/05/2018
ms.keywords: ILegacyIAccessibleProvider interface [Windows Accessibility],SetValue method, ILegacyIAccessibleProvider.SetValue, ILegacyIAccessibleProvider::SetValue, SetValue, SetValue method [Windows Accessibility], SetValue method [Windows Accessibility],ILegacyIAccessibleProvider interface, uiauto.uiauto_ILegacyIAccessibleProvider_SetValue, uiauto_ILegacyIAccessibleProvider_SetValue, uiautomationcore/ILegacyIAccessibleProvider::SetValue, winauto.uiauto_ILegacyIAccessibleProvider_SetValue
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
 - ILegacyIAccessibleProvider::SetValue
 - uiautomationcore/ILegacyIAccessibleProvider::SetValue
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
 - ILegacyIAccessibleProvider.SetValue
---

# ILegacyIAccessibleProvider::SetValue


## -description

Sets the string value of the control.

## -parameters

### -param szValue [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

A localized string that contains the value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ilegacyiaccessibleprovider">ILegacyIAccessibleProvider</a>