---
UID: NF:uiautomationclient.IUIAutomationSelectionItemPattern.RemoveFromSelection
title: IUIAutomationSelectionItemPattern::RemoveFromSelection
author: windows-sdk-content
description: Removes this element from the selection.
old-location: winauto\uiauto_IUIAutomationSelectionItemPattern_RemoveFromSelection.htm
tech.root: WinAuto
ms.assetid: 25f9a8da-4bc9-496e-888c-a270a2bf8fb3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAutomationSelectionItemPattern interface [Windows Accessibility],RemoveFromSelection method, IUIAutomationSelectionItemPattern.RemoveFromSelection, IUIAutomationSelectionItemPattern::RemoveFromSelection, RemoveFromSelection, RemoveFromSelection method [Windows Accessibility], RemoveFromSelection method [Windows Accessibility],IUIAutomationSelectionItemPattern interface, uiauto.uiauto_IUIAutomationSelectionItemPattern_RemoveFromSelection, uiauto_IUIAutomationSelectionItemPattern_RemoveFromSelection, uiautomationclient/IUIAutomationSelectionItemPattern::RemoveFromSelection, winauto.uiauto_IUIAutomationSelectionItemPattern_RemoveFromSelection
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
 - IUIAutomationSelectionItemPattern.RemoveFromSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationSelectionItemPattern::RemoveFromSelection


## -description


Removes this element from the selection.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An error code is returned if this element is the only one in the selection and the selection container requires at least one element to be selected.
			




## -see-also




<a href="https://msdn.microsoft.com/e3d90861-1926-4294-b14b-f4c61a4f9176">AddToSelection</a>



<a href="https://msdn.microsoft.com/608c9b6d-bc53-4d6d-8747-897ac9a24571">CurrentIsSelectionRequired</a>



<a href="https://msdn.microsoft.com/b76d5003-b9af-4a48-91d3-8075f45cf131">IUIAutomationSelectionItemPattern</a>



<a href="https://msdn.microsoft.com/676d3fef-77b8-4f02-9a89-a7471898598f">Select</a>
 

 

