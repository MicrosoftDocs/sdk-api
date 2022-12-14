---
UID: NF:uiautomationclient.IUIAutomationTableItemPattern.GetCachedColumnHeaderItems
title: IUIAutomationTableItemPattern::GetCachedColumnHeaderItems (uiautomationclient.h)
description: Retrieves the cached column headers associated with a table item or cell.
helpviewer_keywords: ["GetCachedColumnHeaderItems","GetCachedColumnHeaderItems method [Windows Accessibility]","GetCachedColumnHeaderItems method [Windows Accessibility]","IUIAutomationTableItemPattern interface","IUIAutomationTableItemPattern interface [Windows Accessibility]","GetCachedColumnHeaderItems method","IUIAutomationTableItemPattern.GetCachedColumnHeaderItems","IUIAutomationTableItemPattern::GetCachedColumnHeaderItems","uiauto.uiauto_IUIAutomationTableItemPattern_GetCachedColumnHeaderItems","uiauto_IUIAutomationTableItemPattern_GetCachedColumnHeaderItems","uiautomationclient/IUIAutomationTableItemPattern::GetCachedColumnHeaderItems","winauto.uiauto_IUIAutomationTableItemPattern_GetCachedColumnHeaderItems"]
old-location: winauto\uiauto_IUIAutomationTableItemPattern_GetCachedColumnHeaderItems.htm
tech.root: WinAuto
ms.assetid: 40d4c31b-643f-479b-859c-3458d2d17f19
ms.date: 12/05/2018
ms.keywords: GetCachedColumnHeaderItems, GetCachedColumnHeaderItems method [Windows Accessibility], GetCachedColumnHeaderItems method [Windows Accessibility],IUIAutomationTableItemPattern interface, IUIAutomationTableItemPattern interface [Windows Accessibility],GetCachedColumnHeaderItems method, IUIAutomationTableItemPattern.GetCachedColumnHeaderItems, IUIAutomationTableItemPattern::GetCachedColumnHeaderItems, uiauto.uiauto_IUIAutomationTableItemPattern_GetCachedColumnHeaderItems, uiauto_IUIAutomationTableItemPattern_GetCachedColumnHeaderItems, uiautomationclient/IUIAutomationTableItemPattern::GetCachedColumnHeaderItems, winauto.uiauto_IUIAutomationTableItemPattern_GetCachedColumnHeaderItems
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
 - IUIAutomationTableItemPattern::GetCachedColumnHeaderItems
 - uiautomationclient/IUIAutomationTableItemPattern::GetCachedColumnHeaderItems
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
 - IUIAutomationTableItemPattern.GetCachedColumnHeaderItems
---

# IUIAutomationTableItemPattern::GetCachedColumnHeaderItems


## -description

Retrieves the cached column headers associated with a table item or cell.

## -parameters

### -param retVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of cached column headers.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtableitempattern">IUIAutomationTableItemPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtableitempattern-getcachedrowheaderitems">IUIAutomationTableItemPattern::GetCachedRowHeaderItems</a>