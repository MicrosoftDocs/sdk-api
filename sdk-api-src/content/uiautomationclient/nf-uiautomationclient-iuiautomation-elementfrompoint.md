---
UID: NF:uiautomationclient.IUIAutomation.ElementFromPoint
title: IUIAutomation::ElementFromPoint
author: windows-sdk-content
description: Retrieves the UI Automation element at the specified point on the desktop.
old-location: winauto\uiauto_IUIAutomation_ElementFromPoint.htm
tech.root: WinAuto
ms.assetid: 4233cc97-94c8-4861-a364-823cca1e5ff8
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ElementFromPoint, ElementFromPoint method [Windows Accessibility], ElementFromPoint method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],ElementFromPoint method, IUIAutomation.ElementFromPoint, IUIAutomation::ElementFromPoint, uiauto.uiauto_IUIAutomation_ElementFromPoint, uiauto_IUIAutomation_ElementFromPoint, uiautomationclient/IUIAutomation::ElementFromPoint, winauto.uiauto_IUIAutomation_ElementFromPoint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::ElementFromPoint


## -description


Retrieves the UI Automation element at the specified point on the desktop.


## -parameters




### -param pt [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

The desktop coordinates of the UI Automation element.


### -param element [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IUIAutomation::ElementFromPoint</b> method returns the <a href="uiauto_error_codes.htm">UIA_E_ELEMENTNOTAVAILABLE</a> error code if the element under the point is already removed by the time the method returns. Clients should handle errors from this method gracefully; for example, by trying the call again. 
			




## -see-also




<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/fb3a8773-270a-4e33-bcbe-bde7794ea4ad">IUIAutomation::ElementFromPointBuildCache</a>
 

 

