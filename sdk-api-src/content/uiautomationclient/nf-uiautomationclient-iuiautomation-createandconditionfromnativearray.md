---
UID: NF:uiautomationclient.IUIAutomation.CreateAndConditionFromNativeArray
title: IUIAutomation::CreateAndConditionFromNativeArray (uiautomationclient.h)
description: Creates a condition that selects elements from a native array, based on multiple conditions that must all be true.
helpviewer_keywords: ["CreateAndConditionFromNativeArray","CreateAndConditionFromNativeArray method [Windows Accessibility]","CreateAndConditionFromNativeArray method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CreateAndConditionFromNativeArray method","IUIAutomation.CreateAndConditionFromNativeArray","IUIAutomation::CreateAndConditionFromNativeArray","uiauto.uiauto_IUIAutomation_CreateAndConditionFromNativeArray","uiauto_IUIAutomation_CreateAndConditionFromNativeArray","uiautomationclient/IUIAutomation::CreateAndConditionFromNativeArray","winauto.uiauto_IUIAutomation_CreateAndConditionFromNativeArray"]
old-location: winauto\uiauto_IUIAutomation_CreateAndConditionFromNativeArray.htm
tech.root: WinAuto
ms.assetid: 2f47dfa7-1558-4984-8400-cac549543819
ms.date: 12/05/2018
ms.keywords: CreateAndConditionFromNativeArray, CreateAndConditionFromNativeArray method [Windows Accessibility], CreateAndConditionFromNativeArray method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateAndConditionFromNativeArray method, IUIAutomation.CreateAndConditionFromNativeArray, IUIAutomation::CreateAndConditionFromNativeArray, uiauto.uiauto_IUIAutomation_CreateAndConditionFromNativeArray, uiauto_IUIAutomation_CreateAndConditionFromNativeArray, uiautomationclient/IUIAutomation::CreateAndConditionFromNativeArray, winauto.uiauto_IUIAutomation_CreateAndConditionFromNativeArray
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
 - IUIAutomation::CreateAndConditionFromNativeArray
 - uiautomationclient/IUIAutomation::CreateAndConditionFromNativeArray
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
 - IUIAutomation.CreateAndConditionFromNativeArray
---

# IUIAutomation::CreateAndConditionFromNativeArray


## -description

Creates a condition that selects elements from a native array, based on multiple conditions that  must all be true.

## -parameters

### -param conditions [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

A pointer to an array of conditions to be combined.

### -param conditionCount [in]

Type: <b>int</b>

The number of elements in the <i>conditions</i> array.

### -param newCondition [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

Receives a pointer to the combined condition.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on each pointer in the <i>conditions</i> array. This means you can call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on those pointers after the call to <b>CreateAndConditionFromNativeArray</b> returns  without invalidating the pointer returned from <b>CreateAndConditionFromNativeArray</b>. When you call <b>Release</b> on the pointer returned from  <b>CreateAndConditionFromNativeArray</b>, UI Automation calls <b>Release</b> on each pointer in the <i>conditions</i> array.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createandcondition">CreateAndCondition</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createandconditionfromarray">CreateAndConditionFromArray</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>



<b>Reference</b>