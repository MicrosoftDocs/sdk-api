---
UID: NF:uiautomationclient.IUIAutomationTablePattern.GetCachedRowHeaders
title: IUIAutomationTablePattern::GetCachedRowHeaders (uiautomationclient.h)
description: Retrieves a cached collection of UI Automation elements representing all the row headers in a table.
helpviewer_keywords: ["GetCachedRowHeaders","GetCachedRowHeaders method [Windows Accessibility]","GetCachedRowHeaders method [Windows Accessibility]","IUIAutomationTablePattern interface","IUIAutomationTablePattern interface [Windows Accessibility]","GetCachedRowHeaders method","IUIAutomationTablePattern.GetCachedRowHeaders","IUIAutomationTablePattern::GetCachedRowHeaders","uiauto.uiauto_IUIAutomationTablePattern_GetCachedRowHeaders","uiauto_IUIAutomationTablePattern_GetCachedRowHeaders","uiautomationclient/IUIAutomationTablePattern::GetCachedRowHeaders","winauto.uiauto_IUIAutomationTablePattern_GetCachedRowHeaders"]
old-location: winauto\uiauto_IUIAutomationTablePattern_GetCachedRowHeaders.htm
tech.root: WinAuto
ms.assetid: 2487f6cd-5871-457d-b634-83bb6191dce2
ms.date: 12/05/2018
ms.keywords: GetCachedRowHeaders, GetCachedRowHeaders method [Windows Accessibility], GetCachedRowHeaders method [Windows Accessibility],IUIAutomationTablePattern interface, IUIAutomationTablePattern interface [Windows Accessibility],GetCachedRowHeaders method, IUIAutomationTablePattern.GetCachedRowHeaders, IUIAutomationTablePattern::GetCachedRowHeaders, uiauto.uiauto_IUIAutomationTablePattern_GetCachedRowHeaders, uiauto_IUIAutomationTablePattern_GetCachedRowHeaders, uiautomationclient/IUIAutomationTablePattern::GetCachedRowHeaders, winauto.uiauto_IUIAutomationTablePattern_GetCachedRowHeaders
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
 - IUIAutomationTablePattern::GetCachedRowHeaders
 - uiautomationclient/IUIAutomationTablePattern::GetCachedRowHeaders
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
 - IUIAutomationTablePattern.GetCachedRowHeaders
---

# IUIAutomationTablePattern::GetCachedRowHeaders


## -description

Retrieves a cached collection of UI Automation elements representing all the row headers in a table.

## -parameters

### -param retVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of cached row headers. The default is an empty array.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtablepattern">IUIAutomationTablePattern</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtablepattern-getcachedcolumnheaders">IUIAutomationTablePattern::GetCachedColumnHeaders</a>