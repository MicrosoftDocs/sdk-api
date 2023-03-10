---
UID: NF:uiautomationclient.IUIAutomationTableItemPattern.GetCachedRowHeaderItems
title: IUIAutomationTableItemPattern::GetCachedRowHeaderItems (uiautomationclient.h)
description: Retrieves the cached row headers associated with a table item or cell.
helpviewer_keywords: ["GetCachedRowHeaderItems","GetCachedRowHeaderItems method [Windows Accessibility]","GetCachedRowHeaderItems method [Windows Accessibility]","IUIAutomationTableItemPattern interface","IUIAutomationTableItemPattern interface [Windows Accessibility]","GetCachedRowHeaderItems method","IUIAutomationTableItemPattern.GetCachedRowHeaderItems","IUIAutomationTableItemPattern::GetCachedRowHeaderItems","uiauto.uiauto_IUIAutomationTableItemPattern_GetCachedRowHeaderItems","uiauto_IUIAutomationTableItemPattern_GetCachedRowHeaderItems","uiautomationclient/IUIAutomationTableItemPattern::GetCachedRowHeaderItems","winauto.uiauto_IUIAutomationTableItemPattern_GetCachedRowHeaderItems"]
old-location: winauto\uiauto_IUIAutomationTableItemPattern_GetCachedRowHeaderItems.htm
tech.root: WinAuto
ms.assetid: 69d4a632-8e35-4569-8c14-f56e9fd84c34
ms.date: 12/05/2018
ms.keywords: GetCachedRowHeaderItems, GetCachedRowHeaderItems method [Windows Accessibility], GetCachedRowHeaderItems method [Windows Accessibility],IUIAutomationTableItemPattern interface, IUIAutomationTableItemPattern interface [Windows Accessibility],GetCachedRowHeaderItems method, IUIAutomationTableItemPattern.GetCachedRowHeaderItems, IUIAutomationTableItemPattern::GetCachedRowHeaderItems, uiauto.uiauto_IUIAutomationTableItemPattern_GetCachedRowHeaderItems, uiauto_IUIAutomationTableItemPattern_GetCachedRowHeaderItems, uiautomationclient/IUIAutomationTableItemPattern::GetCachedRowHeaderItems, winauto.uiauto_IUIAutomationTableItemPattern_GetCachedRowHeaderItems
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
 - IUIAutomationTableItemPattern::GetCachedRowHeaderItems
 - uiautomationclient/IUIAutomationTableItemPattern::GetCachedRowHeaderItems
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
 - IUIAutomationTableItemPattern.GetCachedRowHeaderItems
---

# IUIAutomationTableItemPattern::GetCachedRowHeaderItems


## -description

Retrieves the cached row headers associated with a table item or cell.

## -parameters

### -param retVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of cached row headers.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.