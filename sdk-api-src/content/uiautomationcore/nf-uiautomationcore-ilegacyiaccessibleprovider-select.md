---
UID: NF:uiautomationcore.ILegacyIAccessibleProvider.Select
title: ILegacyIAccessibleProvider::Select (uiautomationcore.h)
description: Selects the element.
helpviewer_keywords: ["ILegacyIAccessibleProvider interface [Windows Accessibility]","Select method","ILegacyIAccessibleProvider.Select","ILegacyIAccessibleProvider::Select","Select","Select method [Windows Accessibility]","Select method [Windows Accessibility]","ILegacyIAccessibleProvider interface","uiauto.uiauto_ILegacyIAccessibleProvider_Select","uiauto_ILegacyIAccessibleProvider_Select","uiautomationcore/ILegacyIAccessibleProvider::Select","winauto.uiauto_ILegacyIAccessibleProvider_Select"]
old-location: winauto\uiauto_ILegacyIAccessibleProvider_Select.htm
tech.root: WinAuto
ms.assetid: 9cdb3f88-c4aa-4a04-94e3-5549c389ad1f
ms.date: 12/05/2018
ms.keywords: ILegacyIAccessibleProvider interface [Windows Accessibility],Select method, ILegacyIAccessibleProvider.Select, ILegacyIAccessibleProvider::Select, Select, Select method [Windows Accessibility], Select method [Windows Accessibility],ILegacyIAccessibleProvider interface, uiauto.uiauto_ILegacyIAccessibleProvider_Select, uiauto_ILegacyIAccessibleProvider_Select, uiautomationcore/ILegacyIAccessibleProvider::Select, winauto.uiauto_ILegacyIAccessibleProvider_Select
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
 - ILegacyIAccessibleProvider::Select
 - uiautomationcore/ILegacyIAccessibleProvider::Select
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
 - ILegacyIAccessibleProvider.Select
---

# ILegacyIAccessibleProvider::Select


## -description

Selects the element.

## -parameters

### -param flagsSelect [in]

Type: <b>long</b>

Specifies which selection or focus operations are to be performed. This parameter must have a combination of the values described in <a href="/windows/desktop/WinAuto/selflag">SELFLAG Constants</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ilegacyiaccessibleprovider">ILegacyIAccessibleProvider</a>