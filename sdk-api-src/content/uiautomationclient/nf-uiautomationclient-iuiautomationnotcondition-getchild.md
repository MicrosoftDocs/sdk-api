---
UID: NF:uiautomationclient.IUIAutomationNotCondition.GetChild
title: IUIAutomationNotCondition::GetChild (uiautomationclient.h)
description: Retrieves the condition of which this condition is the negative.
helpviewer_keywords: ["GetChild","GetChild method [Windows Accessibility]","GetChild method [Windows Accessibility]","IUIAutomationNotCondition interface","IUIAutomationNotCondition interface [Windows Accessibility]","GetChild method","IUIAutomationNotCondition.GetChild","IUIAutomationNotCondition::GetChild","uiauto.uiauto_IUIAutomationNotCondition_GetChild","uiauto_IUIAutomationNotCondition_GetChild","uiautomationclient/IUIAutomationNotCondition::GetChild","winauto.uiauto_IUIAutomationNotCondition_GetChild"]
old-location: winauto\uiauto_IUIAutomationNotCondition_GetChild.htm
tech.root: WinAuto
ms.assetid: 5d3a5df4-045a-41bf-aa98-3e9ac20c1c52
ms.date: 12/05/2018
ms.keywords: GetChild, GetChild method [Windows Accessibility], GetChild method [Windows Accessibility],IUIAutomationNotCondition interface, IUIAutomationNotCondition interface [Windows Accessibility],GetChild method, IUIAutomationNotCondition.GetChild, IUIAutomationNotCondition::GetChild, uiauto.uiauto_IUIAutomationNotCondition_GetChild, uiauto_IUIAutomationNotCondition_GetChild, uiautomationclient/IUIAutomationNotCondition::GetChild, winauto.uiauto_IUIAutomationNotCondition_GetChild
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
 - IUIAutomationNotCondition::GetChild
 - uiautomationclient/IUIAutomationNotCondition::GetChild
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
 - IUIAutomationNotCondition.GetChild
---

# IUIAutomationNotCondition::GetChild


## -description

Retrieves the condition of which this condition is the negative.

## -parameters

### -param condition [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

Receives a pointer to the condition.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The returned condition is the one that was used in creating this condition.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createnotcondition">CreateNotCondition</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationnotcondition">IUIAutomationNotCondition</a>