---
UID: NF:uiautomationclient.IUIAutomationTextRange.MoveEndpointByRange
title: IUIAutomationTextRange::MoveEndpointByRange
author: windows-sdk-content
description: Moves one endpoint of the current text range to the specified endpoint of a second text range.
old-location: winauto\uiauto_IUIAutomationTextRange_MoveEndpointByRange.htm
old-project: WinAuto
ms.assetid: 16cb22ec-2735-41ab-88d5-78a27246af6e
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: IUIAutomationTextRange interface [Windows Accessibility],MoveEndpointByRange method, IUIAutomationTextRange.MoveEndpointByRange, IUIAutomationTextRange::MoveEndpointByRange, MoveEndpointByRange, MoveEndpointByRange method [Windows Accessibility], MoveEndpointByRange method [Windows Accessibility],IUIAutomationTextRange interface, uiauto.uiauto_IUIAutomationTextRange_MoveEndpointByRange, uiauto_IUIAutomationTextRange_MoveEndpointByRange, uiautomationclient/IUIAutomationTextRange::MoveEndpointByRange, winauto.uiauto_IUIAutomationTextRange_MoveEndpointByRange
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationClient.h
api_name:
-	IUIAutomationTextRange.MoveEndpointByRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTextRange::MoveEndpointByRange


## -description


Moves one endpoint of the current text range to the specified endpoint of a second text range.


## -parameters




### -param srcEndPoint [in]

Type: <b><a href="https://msdn.microsoft.com/4a294376-a401-4380-ba5a-b899548290b7">TextPatternRangeEndpoint</a></b>

An endpoint (either start or end) of the current text range. This is the endpoint to be moved.


### -param range [in]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>*</b>

A second text range from the same text provider as the current text range.


### -param targetEndPoint [in]

Type: <b><a href="https://msdn.microsoft.com/4a294376-a401-4380-ba5a-b899548290b7">TextPatternRangeEndpoint</a></b>

An endpoint (either start or end) of the second text range.   The <i>srcEndPoint</i> of the current text range is moved to this endpoint.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the endpoint being moved crosses the other endpoint of the same text range, that other endpoint is moved also, resulting in a degenerate (empty) range and ensuring the correct ordering of the endpoints (that is, the start is always less than or equal to the end).




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

