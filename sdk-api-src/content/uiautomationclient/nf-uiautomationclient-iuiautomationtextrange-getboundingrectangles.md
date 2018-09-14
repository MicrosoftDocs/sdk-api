---
UID: NF:uiautomationclient.IUIAutomationTextRange.GetBoundingRectangles
title: IUIAutomationTextRange::GetBoundingRectangles
author: windows-sdk-content
description: Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range.
old-location: winauto\uiauto_IUIAutomationTextRange_GetBoundingRectangles.htm
tech.root: WinAuto
ms.assetid: a155d143-c5ec-4669-9635-fb8f8012a684
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetBoundingRectangles, GetBoundingRectangles method [Windows Accessibility], GetBoundingRectangles method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],GetBoundingRectangles method, IUIAutomationTextRange.GetBoundingRectangles, IUIAutomationTextRange::GetBoundingRectangles, uiauto.uiauto_IUIAutomationTextRange_GetBoundingRectangles, uiauto_IUIAutomationTextRange_GetBoundingRectangles, uiautomationclient/IUIAutomationTextRange::GetBoundingRectangles, winauto.uiauto_IUIAutomationTextRange_GetBoundingRectangles
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
 - IUIAutomationTextRange.GetBoundingRectangles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextRange::GetBoundingRectangles


## -description


Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range.


## -parameters




### -param boundingRects [out, retval]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a pointer to an array of bounding rectangles for each fully or partially visible line of text in a text range. An empty array is returned for a degenerate (empty) text range or for a text range that is  completely off-screen, scrolled out of view, or obscured by an overlapping window.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For information about how the bounding rectangles are stored in the SAFEARRAY, see <a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/1fa9fad1-55b9-4cb5-a5c2-687074fa5d56">SafeArrayToRectNativeArray</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

