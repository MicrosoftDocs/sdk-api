---
UID: NF:uiautomationclient.IUIAutomation.ElementFromPoint
title: IUIAutomation::ElementFromPoint (uiautomationclient.h)

description: Retrieves the UI Automation element at the specified point on the desktop.
old-location: winauto\uiauto_IUIAutomation_ElementFromPoint.htm
tech.root: WinAuto
ms.assetid: 4233cc97-94c8-4861-a364-823cca1e5ff8

ms.date: 12/05/2018
ms.keywords: ElementFromPoint, ElementFromPoint method [Windows Accessibility], ElementFromPoint method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],ElementFromPoint method, IUIAutomation.ElementFromPoint, IUIAutomation::ElementFromPoint, uiauto.uiauto_IUIAutomation_ElementFromPoint, uiauto_IUIAutomation_ElementFromPoint, uiautomationclient/IUIAutomation::ElementFromPoint, winauto.uiauto_IUIAutomation_ElementFromPoint
ms.topic: method
f1_keywords: 
 - "uiautomationclient/IUIAutomation.ElementFromPoint"
dev_langs:
 - c++
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
 - IUIAutomation.ElementFromPoint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation::ElementFromPoint


## -description


Retrieves the UI Automation element at the specified point on the desktop.


## -parameters




### -param pt [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a></b>

The desktop coordinates of the UI Automation element.


### -param element [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IUIAutomation::ElementFromPoint</b> method returns the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-error-codes">UIA_E_ELEMENTNOTAVAILABLE</a> error code if the element under the point is already removed by the time the method returns. Clients should handle errors from this method gracefully; for example, by trying the call again. 
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache">IUIAutomation::ElementFromPointBuildCache</a>
 

 

