---
UID: NF:uiautomationclient.IUIAutomation.CreateOrCondition
title: IUIAutomation::CreateOrCondition (uiautomationclient.h)
description: Creates a combination of two conditions where a match exists if either of the conditions is true.
helpviewer_keywords: ["CreateOrCondition","CreateOrCondition method [Windows Accessibility]","CreateOrCondition method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CreateOrCondition method","IUIAutomation.CreateOrCondition","IUIAutomation::CreateOrCondition","uiauto.uiauto_IUIAutomation_CreateOrCondition","uiauto_IUIAutomation_CreateOrCondition","uiautomationclient/IUIAutomation::CreateOrCondition","winauto.uiauto_IUIAutomation_CreateOrCondition"]
old-location: winauto\uiauto_IUIAutomation_CreateOrCondition.htm
tech.root: WinAuto
ms.assetid: 17e83b94-21f0-44b6-87be-3fc44b0dc5a0
ms.date: 12/05/2018
ms.keywords: CreateOrCondition, CreateOrCondition method [Windows Accessibility], CreateOrCondition method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateOrCondition method, IUIAutomation.CreateOrCondition, IUIAutomation::CreateOrCondition, uiauto.uiauto_IUIAutomation_CreateOrCondition, uiauto_IUIAutomation_CreateOrCondition, uiautomationclient/IUIAutomation::CreateOrCondition, winauto.uiauto_IUIAutomation_CreateOrCondition
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
 - IUIAutomation::CreateOrCondition
 - uiautomationclient/IUIAutomation::CreateOrCondition
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
 - IUIAutomation.CreateOrCondition
---

# IUIAutomation::CreateOrCondition


## -description

Creates a combination of two conditions where a match exists if either of the conditions is true.

## -parameters

### -param condition1 [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>*</b>

A pointer to the first condition.

### -param condition2 [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>*</b>

A pointer to the second condition.

### -param newCondition [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

Receives a pointer to the combined condition.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>CreateOrCondition</b> method calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the <i>condition1</i> and <i>condition2</i> pointers. This means you can call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on those two pointers after the call to <b>CreateOrCondition</b> returns  without invalidating the pointer returned from <b>CreateOrCondition</b>. When you call <b>Release</b> on the pointer returned from  <b>CreateOrCondition</b>, UI Automation calls <b>Release</b> on the <i>condition1</i> and <i>condition2</i> pointers.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createorconditionfromarray">CreateOrConditionFromArray</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createorconditionfromnativearray">CreateOrConditionFromNativeArray</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>



<b>Reference</b>