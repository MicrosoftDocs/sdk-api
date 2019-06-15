---
UID: NF:uiautomationclient.IUIAutomation.CreateAndConditionFromArray
title: IUIAutomation::CreateAndConditionFromArray (uiautomationclient.h)
author: windows-sdk-content
description: Creates a condition that selects elements based on multiple conditions, all of which must be true.
old-location: winauto\uiauto_IUIAutomation_CreateAndConditionFromArray.htm
tech.root: WinAuto
ms.assetid: ec9ad1a1-72c7-4fc6-8812-577b44b4c5eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateAndConditionFromArray, CreateAndConditionFromArray method [Windows Accessibility], CreateAndConditionFromArray method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateAndConditionFromArray method, IUIAutomation.CreateAndConditionFromArray, IUIAutomation::CreateAndConditionFromArray, uiauto.uiauto_IUIAutomation_CreateAndConditionFromArray, uiauto_IUIAutomation_CreateAndConditionFromArray, uiautomationclient/IUIAutomation::CreateAndConditionFromArray, winauto.uiauto_IUIAutomation_CreateAndConditionFromArray
ms.topic: method
f1_keywords: ["uiautomationclient/IUIAutomation.CreateAndConditionFromArray"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.CreateAndConditionFromArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation::CreateAndConditionFromArray


## -description


Creates a condition that selects elements based on multiple conditions, all of which must be true.


## -parameters




### -param conditions [in]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

A pointer to the conditions to be combined.


### -param newCondition [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

Receives a pointer to the combined condition.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method calls <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on each pointer in the <i>conditions</i> array. This means you can call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on those pointers after the call to <b>CreateAndConditionFromArray</b> returns  without invalidating the pointer returned from <b>CreateAndConditionFromArray</b>. When you call <b>Release</b> on the pointer returned from  <b>CreateAndConditionFromArray</b>, UI Automation calls <b>Release</b> on each pointer in the <i>conditions</i> array.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createandcondition">CreateAndCondition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createandconditionfromnativearray">CreateAndConditionFromNativeArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>



<b>Reference</b>
 

 

