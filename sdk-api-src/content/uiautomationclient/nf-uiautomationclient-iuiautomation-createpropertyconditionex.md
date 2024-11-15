---
UID: NF:uiautomationclient.IUIAutomation.CreatePropertyConditionEx
title: IUIAutomation::CreatePropertyConditionEx (uiautomationclient.h)
description: Creates a condition that selects elements that have a property with the specified value, using optional flags.
helpviewer_keywords: ["CreatePropertyConditionEx","CreatePropertyConditionEx method [Windows Accessibility]","CreatePropertyConditionEx method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CreatePropertyConditionEx method","IUIAutomation.CreatePropertyConditionEx","IUIAutomation::CreatePropertyConditionEx","uiauto.uiauto_IUIAutomation_CreatePropertyConditionEx","uiauto_IUIAutomation_CreatePropertyConditionEx","uiautomationclient/IUIAutomation::CreatePropertyConditionEx","winauto.uiauto_IUIAutomation_CreatePropertyConditionEx"]
old-location: winauto\uiauto_IUIAutomation_CreatePropertyConditionEx.htm
tech.root: WinAuto
ms.assetid: dc7ad9e8-b315-40b1-af02-997a38c4ee66
ms.date: 12/05/2018
ms.keywords: CreatePropertyConditionEx, CreatePropertyConditionEx method [Windows Accessibility], CreatePropertyConditionEx method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreatePropertyConditionEx method, IUIAutomation.CreatePropertyConditionEx, IUIAutomation::CreatePropertyConditionEx, uiauto.uiauto_IUIAutomation_CreatePropertyConditionEx, uiauto_IUIAutomation_CreatePropertyConditionEx, uiautomationclient/IUIAutomation::CreatePropertyConditionEx, winauto.uiauto_IUIAutomation_CreatePropertyConditionEx
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
 - IUIAutomation::CreatePropertyConditionEx
 - uiautomationclient/IUIAutomation::CreatePropertyConditionEx
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
 - IUIAutomation.CreatePropertyConditionEx
---

# IUIAutomation::CreatePropertyConditionEx


## -description

Creates a condition that selects elements that have a property with the specified value, using optional flags.

## -parameters

### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier.  For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param value [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The property value.

### -param flags [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-propertyconditionflags">PropertyConditionFlags</a></b>

The attributes of the condition. Use <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-propertyconditionflags">PropertyConditionFlags_IgnoreCase</a> to create a property condition that is not case-sensitive

### -param newCondition [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

Receives a pointer to the new condition.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createpropertycondition">CreatePropertyCondition</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>



<b>Reference</b>