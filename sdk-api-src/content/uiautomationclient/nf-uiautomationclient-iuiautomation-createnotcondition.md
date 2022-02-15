---
UID: NF:uiautomationclient.IUIAutomation.CreateNotCondition
title: IUIAutomation::CreateNotCondition (uiautomationclient.h)
description: Creates a condition that is the negative of a specified condition.
helpviewer_keywords: ["CreateNotCondition","CreateNotCondition method [Windows Accessibility]","CreateNotCondition method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","CreateNotCondition method","IUIAutomation.CreateNotCondition","IUIAutomation::CreateNotCondition","uiauto.uiauto_IUIAutomation_CreateNotCondition","uiauto_IUIAutomation_CreateNotCondition","uiautomationclient/IUIAutomation::CreateNotCondition","winauto.uiauto_IUIAutomation_CreateNotCondition"]
old-location: winauto\uiauto_IUIAutomation_CreateNotCondition.htm
tech.root: WinAuto
ms.assetid: 183603f9-6e5b-4c44-b6b2-c363b4d150c3
ms.date: 12/05/2018
ms.keywords: CreateNotCondition, CreateNotCondition method [Windows Accessibility], CreateNotCondition method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],CreateNotCondition method, IUIAutomation.CreateNotCondition, IUIAutomation::CreateNotCondition, uiauto.uiauto_IUIAutomation_CreateNotCondition, uiauto_IUIAutomation_CreateNotCondition, uiautomationclient/IUIAutomation::CreateNotCondition, winauto.uiauto_IUIAutomation_CreateNotCondition
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
 - IUIAutomation::CreateNotCondition
 - uiautomationclient/IUIAutomation::CreateNotCondition
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
 - IUIAutomation.CreateNotCondition
---

# IUIAutomation::CreateNotCondition


## -description

Creates a condition that is the negative of a specified condition.

## -parameters

### -param condition [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>*</b>

A pointer to the initial condition.

### -param newCondition [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>**</b>

Receives a pointer to the negative of the initial condition specified by the <i>condition</i> parameter.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>CreateNotCondition</b> method calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the <i>condition</i> pointer. This means you can call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on that pointer after the call to <b>CreateNotCondition</b> returns  without invalidating the pointer returned from <b>CreateNotCondition</b>. When you call <b>Release</b> on the pointer returned from  <b>CreateNotCondition</b>, UI Automation calls <b>Release</b> on the <i>condition</i> pointer.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>



<b>Reference</b>