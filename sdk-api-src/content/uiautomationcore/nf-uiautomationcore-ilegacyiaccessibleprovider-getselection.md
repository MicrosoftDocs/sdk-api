---
UID: NF:uiautomationcore.ILegacyIAccessibleProvider.GetSelection
title: ILegacyIAccessibleProvider::GetSelection (uiautomationcore.h)
description: Retrieves the selected item or items in the control.
helpviewer_keywords: ["GetSelection","GetSelection method [Windows Accessibility]","GetSelection method [Windows Accessibility]","ILegacyIAccessibleProvider interface","ILegacyIAccessibleProvider interface [Windows Accessibility]","GetSelection method","ILegacyIAccessibleProvider.GetSelection","ILegacyIAccessibleProvider::GetSelection","uiauto.uiauto_ILegacyIAccessibleProvider_GetSelection","uiauto_ILegacyIAccessibleProvider_GetSelection","uiautomationcore/ILegacyIAccessibleProvider::GetSelection","winauto.uiauto_ILegacyIAccessibleProvider_GetSelection"]
old-location: winauto\uiauto_ILegacyIAccessibleProvider_GetSelection.htm
tech.root: WinAuto
ms.assetid: 8436e554-2f09-46ed-a32a-0d2612bc60fb
ms.date: 12/05/2018
ms.keywords: GetSelection, GetSelection method [Windows Accessibility], GetSelection method [Windows Accessibility],ILegacyIAccessibleProvider interface, ILegacyIAccessibleProvider interface [Windows Accessibility],GetSelection method, ILegacyIAccessibleProvider.GetSelection, ILegacyIAccessibleProvider::GetSelection, uiauto.uiauto_ILegacyIAccessibleProvider_GetSelection, uiauto_ILegacyIAccessibleProvider_GetSelection, uiautomationcore/ILegacyIAccessibleProvider::GetSelection, winauto.uiauto_ILegacyIAccessibleProvider_GetSelection
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
 - ILegacyIAccessibleProvider::GetSelection
 - uiautomationcore/ILegacyIAccessibleProvider::GetSelection
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
 - ILegacyIAccessibleProvider.GetSelection
---

# ILegacyIAccessibleProvider::GetSelection


## -description

Retrieves the selected item or items in the control.

## -parameters

### -param pvarSelectedChildren [out]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to a <a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> containing the selected items.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ilegacyiaccessibleprovider">ILegacyIAccessibleProvider</a>



<b>Reference</b>