---
UID: NF:rtscom.IRealTimeStylus.GetTablet
title: IRealTimeStylus::GetTablet (rtscom.h)
description: Retrieves an IInkTablet Interface object to the caller.
helpviewer_keywords: ["38970fc0-ec4c-4068-a146-83edaa040c8c","GetTablet","GetTablet method [Tablet PC]","GetTablet method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","GetTablet method","IRealTimeStylus.GetTablet","IRealTimeStylus::GetTablet","rtscom/IRealTimeStylus::GetTablet","tablet.irealtimestylus_gettablet"]
old-location: tablet\irealtimestylus_gettablet.htm
tech.root: tablet
ms.assetid: 38970fc0-ec4c-4068-a146-83edaa040c8c
ms.date: 12/05/2018
ms.keywords: 38970fc0-ec4c-4068-a146-83edaa040c8c, GetTablet, GetTablet method [Tablet PC], GetTablet method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetTablet method, IRealTimeStylus.GetTablet, IRealTimeStylus::GetTablet, rtscom/IRealTimeStylus::GetTablet, tablet.irealtimestylus_gettablet
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
 - IRealTimeStylus::GetTablet
 - rtscom/IRealTimeStylus::GetTablet
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
 - IRealTimeStylus.GetTablet
---

# IRealTimeStylus::GetTablet


## -description

Retrieves an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a> object to the caller.

## -parameters

### -param ppiSingleTablet [out, retval]

A pointer to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a> object.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

This method returns, <i>ppiSingleTablet</i> will contain <b>NULL</b> when the RealTimeStylus is receiving data from more that one tablet. For instance, when the <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setalltabletsmode">IRealTimeStylus::SetAllTabletsMode Method</a> is called with a value of <b>TRUE</b> on a machine with a digitizer and mouse.


#### Examples

The following C++ example code gets a pointer to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a> object and uses that pointer to get the tablet's Plug and Play identifier.


```cpp
// Must be in single tablet mode for GetTablet to succeed. This call to
// SetSingleTabletMode() would likely happen somewhere else in the app.
if (SUCCEEDED(g_pRealTimeStylus->SetSingleTabletMode(pInkTablet)))
{
    IInkTablet* pTablet = NULL;

    if ((SUCCEEDED(g_pRealTimeStylus->GetTablet(&pTablet))) && (NULL != pTablet))
    {
        BSTR bstrPnPID;

        if (SUCCEEDED(pTablet->get_PlugAndPlayId(&bstrPnPID)))
        {
            TRACE("The tablet's Plug-n-Play ID is: %s\n", bstrPnPID);
        }
    }

    // Restore all tablets mode.
    g_pRealTimeStylus->SetAllTabletsMode(TRUE);
}

```

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<b>RealTimeStylus Class</b>