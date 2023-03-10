---
UID: NF:uiautomationclient.IUIAutomationTextRange.GetChildren
title: IUIAutomationTextRange::GetChildren (uiautomationclient.h)
description: Retrieves a collection of all embedded objects that fall within the text range. (IUIAutomationTextRange.GetChildren)
helpviewer_keywords: ["GetChildren","GetChildren method [Windows Accessibility]","GetChildren method [Windows Accessibility]","IUIAutomationTextRange interface","IUIAutomationTextRange interface [Windows Accessibility]","GetChildren method","IUIAutomationTextRange.GetChildren","IUIAutomationTextRange::GetChildren","uiauto.uiauto_IUIAutomationTextRange_GetChildren","uiauto_IUIAutomationTextRange_GetChildren","uiautomationclient/IUIAutomationTextRange::GetChildren","winauto.uiauto_IUIAutomationTextRange_GetChildren"]
old-location: winauto\uiauto_IUIAutomationTextRange_GetChildren.htm
tech.root: WinAuto
ms.assetid: 714e9d91-c6b9-4fa2-8a14-9bdd721b3135
ms.date: 12/05/2018
ms.keywords: GetChildren, GetChildren method [Windows Accessibility], GetChildren method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],GetChildren method, IUIAutomationTextRange.GetChildren, IUIAutomationTextRange::GetChildren, uiauto.uiauto_IUIAutomationTextRange_GetChildren, uiauto_IUIAutomationTextRange_GetChildren, uiautomationclient/IUIAutomationTextRange::GetChildren, winauto.uiauto_IUIAutomationTextRange_GetChildren
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
 - IUIAutomationTextRange::GetChildren
 - uiautomationclient/IUIAutomationTextRange::GetChildren
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
 - IUIAutomationTextRange.GetChildren
---

# IUIAutomationTextRange::GetChildren


## -description

Retrieves a collection of all embedded objects that fall within the text range.

## -parameters

### -param children [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of all child objects that fall within the range. Children that overlap with the range but are not entirely enclosed by it are also included in the collection. An empty collection is returned if there are no child objects.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
