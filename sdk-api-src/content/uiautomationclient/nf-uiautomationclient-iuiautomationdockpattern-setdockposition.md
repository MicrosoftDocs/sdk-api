---
UID: NF:uiautomationclient.IUIAutomationDockPattern.SetDockPosition
title: IUIAutomationDockPattern::SetDockPosition (uiautomationclient.h)
description: Sets the dock position of this element.
helpviewer_keywords: ["IUIAutomationDockPattern interface [Windows Accessibility]","SetDockPosition method","IUIAutomationDockPattern.SetDockPosition","IUIAutomationDockPattern::SetDockPosition","SetDockPosition","SetDockPosition method [Windows Accessibility]","SetDockPosition method [Windows Accessibility]","IUIAutomationDockPattern interface","uiauto.uiauto_IUIAutomationDockPattern_SetDockPosition","uiauto_IUIAutomationDockPattern_SetDockPosition","uiautomationclient/IUIAutomationDockPattern::SetDockPosition","winauto.uiauto_IUIAutomationDockPattern_SetDockPosition"]
old-location: winauto\uiauto_IUIAutomationDockPattern_SetDockPosition.htm
tech.root: WinAuto
ms.assetid: 165de0f3-61b3-473c-8f97-3070596451db
ms.date: 12/05/2018
ms.keywords: IUIAutomationDockPattern interface [Windows Accessibility],SetDockPosition method, IUIAutomationDockPattern.SetDockPosition, IUIAutomationDockPattern::SetDockPosition, SetDockPosition, SetDockPosition method [Windows Accessibility], SetDockPosition method [Windows Accessibility],IUIAutomationDockPattern interface, uiauto.uiauto_IUIAutomationDockPattern_SetDockPosition, uiauto_IUIAutomationDockPattern_SetDockPosition, uiautomationclient/IUIAutomationDockPattern::SetDockPosition, winauto.uiauto_IUIAutomationDockPattern_SetDockPosition
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
 - IUIAutomationDockPattern::SetDockPosition
 - uiautomationclient/IUIAutomationDockPattern::SetDockPosition
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
 - IUIAutomationDockPattern.SetDockPosition
---

# IUIAutomationDockPattern::SetDockPosition


## -description

Sets the dock position of this element.

## -parameters

### -param dockPos [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-dockposition">DockPosition</a></b>

The new dock position.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationdockpattern">IUIAutomationDockPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationdockpattern-get_currentdockposition">IUIAutomationDockPattern::CurrentDockPosition</a>