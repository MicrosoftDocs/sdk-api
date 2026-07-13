---
UID: NF:uiautomationclient.IUIAutomation.GetPatternProgrammaticName
title: IUIAutomation::GetPatternProgrammaticName (uiautomationclient.h)
description: Retrieves the registered programmatic name of a control pattern.
helpviewer_keywords: ["GetPatternProgrammaticName","GetPatternProgrammaticName method [Windows Accessibility]","GetPatternProgrammaticName method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","GetPatternProgrammaticName method","IUIAutomation.GetPatternProgrammaticName","IUIAutomation::GetPatternProgrammaticName","uiauto.uiauto_IUIAutomation_GetPatternProgrammaticName","uiauto_IUIAutomation_GetPatternProgrammaticName","uiautomationclient/IUIAutomation::GetPatternProgrammaticName","winauto.uiauto_IUIAutomation_GetPatternProgrammaticName"]
old-location: winauto\uiauto_IUIAutomation_GetPatternProgrammaticName.htm
tech.root: WinAuto
ms.assetid: a5968193-e3d9-41d1-b13f-8e86db5e0c70
ms.date: 12/05/2018
ms.keywords: GetPatternProgrammaticName, GetPatternProgrammaticName method [Windows Accessibility], GetPatternProgrammaticName method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],GetPatternProgrammaticName method, IUIAutomation.GetPatternProgrammaticName, IUIAutomation::GetPatternProgrammaticName, uiauto.uiauto_IUIAutomation_GetPatternProgrammaticName, uiauto_IUIAutomation_GetPatternProgrammaticName, uiautomationclient/IUIAutomation::GetPatternProgrammaticName, winauto.uiauto_IUIAutomation_GetPatternProgrammaticName
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - IUIAutomation::GetPatternProgrammaticName
 - uiautomationclient/IUIAutomation::GetPatternProgrammaticName
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
 - IUIAutomation.GetPatternProgrammaticName
---

# IUIAutomation::GetPatternProgrammaticName


## -description

Retrieves the registered programmatic name of a control pattern.

## -parameters

### -param pattern [in]

Type: <b>PATTERNID</b>

The identifier of the control pattern. For a list of control pattern IDs, see <a href="/windows/desktop/WinAuto/uiauto-controlpattern-ids">Control Pattern Identifiers</a>.

### -param name [out, retval]

Type: <b>BSTR*</b>

Receives the registered programmatic name.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The programmatic name is intended for debugging and diagnostic purposes only. The string is not localized.

This property should not be used in string comparisons. To determine whether two control patterns are the same, compare the control pattern identifiers directly.