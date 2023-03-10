---
UID: NF:uiautomationcoreapi.LegacyIAccessiblePattern_GetIAccessible
title: LegacyIAccessiblePattern_GetIAccessible function (uiautomationcoreapi.h)
description: Retrieves an IAccessible object that corresponds to the UI Automation element.
helpviewer_keywords: ["LegacyIAccessiblePattern_GetIAccessible","LegacyIAccessiblePattern_GetIAccessible function [Windows Accessibility]","uiauto.uiauto_LegacyIAccessiblePattern_GetIAccessibleConPat","uiauto_LegacyIAccessiblePattern_GetIAccessibleConPat","uiautomationcoreapi/LegacyIAccessiblePattern_GetIAccessible","winauto.uiauto_LegacyIAccessiblePattern_GetIAccessibleConPat"]
old-location: winauto\uiauto_LegacyIAccessiblePattern_GetIAccessibleConPat.htm
tech.root: WinAuto
ms.assetid: 4f05dae6-d315-457c-a496-fe915dd00265
ms.date: 12/05/2018
ms.keywords: LegacyIAccessiblePattern_GetIAccessible, LegacyIAccessiblePattern_GetIAccessible function [Windows Accessibility], uiauto.uiauto_LegacyIAccessiblePattern_GetIAccessibleConPat, uiauto_LegacyIAccessiblePattern_GetIAccessibleConPat, uiautomationcoreapi/LegacyIAccessiblePattern_GetIAccessible, winauto.uiauto_LegacyIAccessiblePattern_GetIAccessibleConPat
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LegacyIAccessiblePattern_GetIAccessible
 - uiautomationcoreapi/LegacyIAccessiblePattern_GetIAccessible
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - LegacyIAccessiblePattern_GetIAccessible
---

# LegacyIAccessiblePattern_GetIAccessible function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> object that corresponds to the UI Automation element.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

A control pattern object.

### -param pAccessible [out]

Type: <b><a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>**</b>

The address of a variable that receives a pointer to an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface for the accessible object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.