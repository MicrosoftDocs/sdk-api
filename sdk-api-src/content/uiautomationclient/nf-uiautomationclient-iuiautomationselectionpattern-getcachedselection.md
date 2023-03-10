---
UID: NF:uiautomationclient.IUIAutomationSelectionPattern.GetCachedSelection
title: IUIAutomationSelectionPattern::GetCachedSelection (uiautomationclient.h)
description: Retrieves the cached selected elements in the container.
helpviewer_keywords: ["GetCachedSelection","GetCachedSelection method [Windows Accessibility]","GetCachedSelection method [Windows Accessibility]","IUIAutomationSelectionPattern interface","IUIAutomationSelectionPattern interface [Windows Accessibility]","GetCachedSelection method","IUIAutomationSelectionPattern.GetCachedSelection","IUIAutomationSelectionPattern::GetCachedSelection","uiauto.uiauto_IUIAutomationSelectionPattern_GetCachedSelection","uiauto_IUIAutomationSelectionPattern_GetCachedSelection","uiautomationclient/IUIAutomationSelectionPattern::GetCachedSelection","winauto.uiauto_IUIAutomationSelectionPattern_GetCachedSelection"]
old-location: winauto\uiauto_IUIAutomationSelectionPattern_GetCachedSelection.htm
tech.root: WinAuto
ms.assetid: a0f2d198-78a9-4117-9a55-aa9042ef3f21
ms.date: 12/05/2018
ms.keywords: GetCachedSelection, GetCachedSelection method [Windows Accessibility], GetCachedSelection method [Windows Accessibility],IUIAutomationSelectionPattern interface, IUIAutomationSelectionPattern interface [Windows Accessibility],GetCachedSelection method, IUIAutomationSelectionPattern.GetCachedSelection, IUIAutomationSelectionPattern::GetCachedSelection, uiauto.uiauto_IUIAutomationSelectionPattern_GetCachedSelection, uiauto_IUIAutomationSelectionPattern_GetCachedSelection, uiautomationclient/IUIAutomationSelectionPattern::GetCachedSelection, winauto.uiauto_IUIAutomationSelectionPattern_GetCachedSelection
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
 - IUIAutomationSelectionPattern::GetCachedSelection
 - uiautomationclient/IUIAutomationSelectionPattern::GetCachedSelection
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
 - IUIAutomationSelectionPattern.GetCachedSelection
---

# IUIAutomationSelectionPattern::GetCachedSelection


## -description

Retrieves the cached selected elements in the container.

## -parameters

### -param retVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to the cached collection of selected elements. The default is an empty array.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationselectionpattern">IUIAutomationSelectionPattern</a>