---
UID: NF:rtscom.IRealTimeStylus.ClearStylusQueues
title: IRealTimeStylus::ClearStylusQueues (rtscom.h)
author: windows-sdk-content
description: Clears the RealTimeStylus Class input and output queues of data.
old-location: tablet\irealtimestylus_clearstylusqueues.htm
tech.root: tablet
ms.assetid: 28270403-9d6d-4e57-9ec5-0d697f4df185
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 28270403-9d6d-4e57-9ec5-0d697f4df185, ClearStylusQueues, ClearStylusQueues method [Tablet PC], ClearStylusQueues method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],ClearStylusQueues method, IRealTimeStylus.ClearStylusQueues, IRealTimeStylus::ClearStylusQueues, rtscom/IRealTimeStylus::ClearStylusQueues, tablet.irealtimestylus_clearstylusqueues
ms.topic: method
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus.ClearStylusQueues
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRealTimeStylus::ClearStylusQueues


## -description



Clears the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> input and output queues of data.




## -parameters






## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



The <b>ClearStylusQueues</b> method can be used to quickly clear the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> queues. This method clears the queues of all data.


#### Examples

The following C++ example code snippet shows a button click event handler that calls <b>IRealTimeStylus::ClearStylusQueues Method</b>. It also redraws the window where a <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer</a> object has been drawing ink.


```cpp
void CCOMRTSDlg::OnBnClickedButtonClearTestArea()
{
	// Clear the stylus queues
	if (!SUCCEEDED(g_pRealTimeStylus->ClearStylusQueues()))
	{
		TRACE("Error clearing stylus queues.");
	}

	// Clear the status text
	m_staticGestureStatus.SetWindowTextW(L"");

	// Redaw the window to clear the ink
	this->RedrawWindow();
}

```





## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture Control Reference</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

