---
UID: NF:uiautomationclient.IUIAutomation.CreateAndCondition
title: IUIAutomation::CreateAndCondition (uiautomationclient.h)
description: Creates a condition that selects elements that match both of two conditions.
helpviewer_keywords: ["CreateAndCondition","CreateAndCondition method [Windows Accessibility]","CreateAndCondition method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CreateAndCondition method","IUIAutomation.CreateAndCondition","IUIAutomation::CreateAndCondition","uiauto.uiauto_IUIAutomation_CreateAndCondition","uiauto_IUIAutomation_CreateAndCondition","uiautomationclient/IUIAutomation::CreateAndCondition","winauto.uiauto_IUIAutomation_CreateAndCondition"]
old-location: winauto\uiauto_IUIAutomation_CreateAndCondition.htm
tech.root: WinAuto
ms.assetid: 066476b4-586c-477c-82ee-de2f2074d63b
ms.date: 12/05/2018
ms.keywords: CreateAndCondition, CreateAndCondition method [Windows Accessibility], CreateAndCondition method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateAndCondition method, IUIAutomation.CreateAndCondition, IUIAutomation::CreateAndCondition, uiauto.uiauto_IUIAutomation_CreateAndCondition, uiauto_IUIAutomation_CreateAndCondition, uiautomationclient/IUIAutomation::CreateAndCondition, winauto.uiauto_IUIAutomation_CreateAndCondition
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
 - IUIAutomation::CreateAndCondition
 - uiautomationclient/IUIAutomation::CreateAndCondition
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
 - IUIAutomation.CreateAndCondition
---

# IUIAutomation::CreateAndCondition


## -description

Creates a condition that selects elements that match both of two conditions.

## -parameters

### -param condition1 [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>*</b>

A pointer to the first condition to match.

### -param condition2 [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>*</b>

A pointer to the second condition to match.

### -param newCondition [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

Receives a pointer to the combined condition.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A condition that combines more than two simple conditions can be created by using <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createandconditionfromarray">IUIAutomation::CreateAndConditionFromArray</a> or <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createandconditionfromnativearray">IUIAutomation::CreateAndConditionFromNativeArray</a>.


The <b>CreateAndCondition</b> method calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the <i>condition1</i> and <i>condition2</i> pointers. This means you can call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on those two pointers after the call to <b>CreateAndCondition</b> returns  without invalidating the pointer returned from <b>CreateAndCondition</b>. When you call <b>Release</b> on the pointer returned from  <b>CreateAndCondition</b>, UI Automation calls <b>Release</b> on the <i>condition1</i> and <i>condition2</i> pointers.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createandconditionfromarray">CreateAndConditionFromArray</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>



<b>Reference</b>