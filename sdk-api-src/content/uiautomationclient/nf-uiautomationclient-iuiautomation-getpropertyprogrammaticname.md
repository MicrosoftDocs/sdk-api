---
UID: NF:uiautomationclient.IUIAutomation.GetPropertyProgrammaticName
title: IUIAutomation::GetPropertyProgrammaticName (uiautomationclient.h)
description: Retrieves the registered programmatic name of a property.
helpviewer_keywords: ["GetPropertyProgrammaticName","GetPropertyProgrammaticName method [Windows Accessibility]","GetPropertyProgrammaticName method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","GetPropertyProgrammaticName method","IUIAutomation.GetPropertyProgrammaticName","IUIAutomation::GetPropertyProgrammaticName","uiauto.uiauto_IUIAutomation_GetPropertyProgrammaticName","uiauto_IUIAutomation_GetPropertyProgrammaticName","uiautomationclient/IUIAutomation::GetPropertyProgrammaticName","winauto.uiauto_IUIAutomation_GetPropertyProgrammaticName"]
old-location: winauto\uiauto_IUIAutomation_GetPropertyProgrammaticName.htm
tech.root: WinAuto
ms.assetid: f4472de0-7194-411d-a508-a5d81aba8b7d
ms.date: 12/05/2018
ms.keywords: GetPropertyProgrammaticName, GetPropertyProgrammaticName method [Windows Accessibility], GetPropertyProgrammaticName method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],GetPropertyProgrammaticName method, IUIAutomation.GetPropertyProgrammaticName, IUIAutomation::GetPropertyProgrammaticName, uiauto.uiauto_IUIAutomation_GetPropertyProgrammaticName, uiauto_IUIAutomation_GetPropertyProgrammaticName, uiautomationclient/IUIAutomation::GetPropertyProgrammaticName, winauto.uiauto_IUIAutomation_GetPropertyProgrammaticName
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
 - IUIAutomation::GetPropertyProgrammaticName
 - uiautomationclient/IUIAutomation::GetPropertyProgrammaticName
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
 - IUIAutomation.GetPropertyProgrammaticName
---

# IUIAutomation::GetPropertyProgrammaticName


## -description

Retrieves the registered programmatic name of a property.

## -parameters

### -param property [in]

Type: <b>PROPERTYID</b>

The property identifier.  For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param name [out, retval]

Type: <b>BSTR*</b>

Receives the registered programmatic name.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The programmatic name is intended for debugging and diagnostic purposes only. The string is not localized.

This property should not be used in string comparisons. To determine whether two properties are the same, compare the property identifiers directly.