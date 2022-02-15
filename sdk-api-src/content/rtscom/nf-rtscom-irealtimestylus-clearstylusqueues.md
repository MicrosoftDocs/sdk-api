---
UID: NF:rtscom.IRealTimeStylus.ClearStylusQueues
title: IRealTimeStylus::ClearStylusQueues (rtscom.h)
description: Clears the RealTimeStylus Class input and output queues of data.
helpviewer_keywords: ["28270403-9d6d-4e57-9ec5-0d697f4df185","ClearStylusQueues","ClearStylusQueues method [Tablet PC]","ClearStylusQueues method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","ClearStylusQueues method","IRealTimeStylus.ClearStylusQueues","IRealTimeStylus::ClearStylusQueues","rtscom/IRealTimeStylus::ClearStylusQueues","tablet.irealtimestylus_clearstylusqueues"]
old-location: tablet\irealtimestylus_clearstylusqueues.htm
tech.root: tablet
ms.assetid: 28270403-9d6d-4e57-9ec5-0d697f4df185
ms.date: 12/05/2018
ms.keywords: 28270403-9d6d-4e57-9ec5-0d697f4df185, ClearStylusQueues, ClearStylusQueues method [Tablet PC], ClearStylusQueues method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],ClearStylusQueues method, IRealTimeStylus.ClearStylusQueues, IRealTimeStylus::ClearStylusQueues, rtscom/IRealTimeStylus::ClearStylusQueues, tablet.irealtimestylus_clearstylusqueues
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRealTimeStylus::ClearStylusQueues
 - rtscom/IRealTimeStylus::ClearStylusQueues
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus.ClearStylusQueues
---

# IRealTimeStylus::ClearStylusQueues


## -description

Clears the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> input and output queues of data.



## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

The <b>ClearStylusQueues</b> method can be used to quickly clear the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> queues. This method clears the queues of all data.


#### Examples

The following C++ example code snippet shows a button click event handler that calls <b>IRealTimeStylus::ClearStylusQueues Method</b>. It also redraws the window where a <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer</a> object has been drawing ink.


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

	// Redraw the window to clear the ink
	this->RedrawWindow();
}

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture Control Reference</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>
