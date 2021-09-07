---
UID: NF:uiautomationclient.IUIAutomation.CreateOrConditionFromArray
title: IUIAutomation::CreateOrConditionFromArray (uiautomationclient.h)
description: Creates a combination of two or more conditions where a match exists if any of the conditions is true.
helpviewer_keywords: ["CreateOrConditionFromArray","CreateOrConditionFromArray method [Windows Accessibility]","CreateOrConditionFromArray method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CreateOrConditionFromArray method","IUIAutomation.CreateOrConditionFromArray","IUIAutomation::CreateOrConditionFromArray","uiauto.uiauto_IUIAutomation_CreateOrConditionFromArray","uiauto_IUIAutomation_CreateOrConditionFromArray","uiautomationclient/IUIAutomation::CreateOrConditionFromArray","winauto.uiauto_IUIAutomation_CreateOrConditionFromArray"]
old-location: winauto\uiauto_IUIAutomation_CreateOrConditionFromArray.htm
tech.root: WinAuto
ms.assetid: acd15fd0-ac15-4477-8e89-4d7a4f9c93c6
ms.date: 12/05/2018
ms.keywords: CreateOrConditionFromArray, CreateOrConditionFromArray method [Windows Accessibility], CreateOrConditionFromArray method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateOrConditionFromArray method, IUIAutomation.CreateOrConditionFromArray, IUIAutomation::CreateOrConditionFromArray, uiauto.uiauto_IUIAutomation_CreateOrConditionFromArray, uiauto_IUIAutomation_CreateOrConditionFromArray, uiautomationclient/IUIAutomation::CreateOrConditionFromArray, winauto.uiauto_IUIAutomation_CreateOrConditionFromArray
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
 - IUIAutomation::CreateOrConditionFromArray
 - uiautomationclient/IUIAutomation::CreateOrConditionFromArray
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
 - IUIAutomation.CreateOrConditionFromArray
---

# IUIAutomation::CreateOrConditionFromArray


## -description

Creates a combination of two or more conditions where a match exists if any of the conditions is true.

## -parameters

### -param conditions [in]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>*</b>

A pointer to the conditions.

### -param newCondition [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

Receives a pointer to the combined condition.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on each pointer in the <i>conditions</i> array. This means you can call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on those pointers after the call to <b>CreateOrConditionFromArray</b> returns  without invalidating the pointer returned from <b>CreateOrConditionFromArray</b>. When you call <b>Release</b> on the pointer returned from  <b>CreateOrConditionFromArray</b>, UI Automation calls <b>Release</b> on each pointer in the <i>conditions</i> array.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createorcondition">CreateOrCondition</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createorconditionfromnativearray">CreateOrConditionFromNativeArray</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>



<b>Reference</b>