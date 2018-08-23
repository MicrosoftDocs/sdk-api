---
UID: NF:uiautomationcore.ITextRangeProvider.MoveEndpointByRange
title: ITextRangeProvider::MoveEndpointByRange
author: windows-sdk-content
description: Moves one endpoint of the current text range to the specified endpoint of a second text range.
old-location: winauto\uiauto_ITextRangeProvider_MoveEndpointByRange.htm
old-project: WinAuto
ms.assetid: 86411603-c37f-4192-95d1-8ac9b6ab6c44
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextRangeProvider interface [Windows Accessibility],MoveEndpointByRange method, ITextRangeProvider.MoveEndpointByRange, ITextRangeProvider::MoveEndpointByRange, MoveEndpointByRange, MoveEndpointByRange method [Windows Accessibility], MoveEndpointByRange method [Windows Accessibility],ITextRangeProvider interface, uiauto.uiauto_ITextRangeProvider_MoveEndpointByRange, uiauto_ITextRangeProvider_MoveEndpointByRange, uiautomationcore/ITextRangeProvider::MoveEndpointByRange, winauto.uiauto_ITextRangeProvider_MoveEndpointByRange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextRangeProvider.MoveEndpointByRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRangeProvider::MoveEndpointByRange


## -description


Moves one endpoint of the current text range to the specified endpoint of a second text range.  
		


## -parameters




### -param param






### -param targetRange [in]

Type: <b><a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>*</b>

A second text range from the same text provider as the current text range.


#### - endpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

An endpoint (either start or end) of the current text range. This is the endpoint to be moved.


#### - targetEndpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

An endpoint (either start or end) of the second text range.   The <i>endpoint</i> of the current text range is moved to this endpoint.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the endpoint being moved crosses the other endpoint of the same text range, that other endpoint is moved also, resulting in a degenerate (empty) range and ensuring the correct ordering of the endpoints (that is, the start is always less than or equal to the end).




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

