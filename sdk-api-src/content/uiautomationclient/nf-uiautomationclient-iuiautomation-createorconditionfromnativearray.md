---
UID: NF:uiautomationclient.IUIAutomation.CreateOrConditionFromNativeArray
title: IUIAutomation::CreateOrConditionFromNativeArray (uiautomationclient.h)
description: Creates a combination of two or more conditions where a match exists if any one of the conditions is true.
helpviewer_keywords: ["CreateOrConditionFromNativeArray","CreateOrConditionFromNativeArray method [Windows Accessibility]","CreateOrConditionFromNativeArray method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CreateOrConditionFromNativeArray method","IUIAutomation.CreateOrConditionFromNativeArray","IUIAutomation::CreateOrConditionFromNativeArray","uiauto.uiauto_IUIAutomation_CreateOrConditionFromNativeArray","uiauto_IUIAutomation_CreateOrConditionFromNativeArray","uiautomationclient/IUIAutomation::CreateOrConditionFromNativeArray","winauto.uiauto_IUIAutomation_CreateOrConditionFromNativeArray"]
old-location: winauto\uiauto_IUIAutomation_CreateOrConditionFromNativeArray.htm
tech.root: WinAuto
ms.assetid: 393c777c-f262-462b-ac59-035f590bee1c
ms.date: 12/05/2018
ms.keywords: CreateOrConditionFromNativeArray, CreateOrConditionFromNativeArray method [Windows Accessibility], CreateOrConditionFromNativeArray method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateOrConditionFromNativeArray method, IUIAutomation.CreateOrConditionFromNativeArray, IUIAutomation::CreateOrConditionFromNativeArray, uiauto.uiauto_IUIAutomation_CreateOrConditionFromNativeArray, uiauto_IUIAutomation_CreateOrConditionFromNativeArray, uiautomationclient/IUIAutomation::CreateOrConditionFromNativeArray, winauto.uiauto_IUIAutomation_CreateOrConditionFromNativeArray
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
 - IUIAutomation::CreateOrConditionFromNativeArray
 - uiautomationclient/IUIAutomation::CreateOrConditionFromNativeArray
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
 - IUIAutomation.CreateOrConditionFromNativeArray
---

# IUIAutomation::CreateOrConditionFromNativeArray


## -description

Creates a combination of two or more conditions where a match exists if any one of the conditions is true.

## -parameters

### -param conditions [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

A pointer to an array of conditions to combine.

### -param conditionCount [in]

Type: <b>int</b>

The number of elements in <i>conditions</i>.

### -param newCondition [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

Receives a pointer to the combined condition.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on each pointer in the <i>conditions</i> array. This means you can call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on those pointers after the call to <b>CreateOrConditionFromNativeArray</b> returns  without invalidating the pointer returned from <b>CreateOrConditionFromNativeArray</b>. When you call <b>Release</b> on the pointer returned from  <b>CreateOrConditionFromNativeArray</b>, UI Automation calls <b>Release</b> on each pointer in the <i>conditions</i> array.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createorcondition">CreateOrCondition</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createorconditionfromarray">CreateOrConditionFromArray</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>



<b>Reference</b>