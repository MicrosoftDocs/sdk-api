---
UID: NF:rtscom.IRealTimeStylus.GetTabletContextIdFromTablet
title: IRealTimeStylus::GetTabletContextIdFromTablet (rtscom.h)
description: Retrieves the TabletContextId property that is associated with a given tablet digitizer object.
helpviewer_keywords: ["9f4cc882-c25f-4862-8b78-4db108d0b5d4","GetTabletContextIdFromTablet","GetTabletContextIdFromTablet method [Tablet PC]","GetTabletContextIdFromTablet method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","GetTabletContextIdFromTablet method","IRealTimeStylus.GetTabletContextIdFromTablet","IRealTimeStylus::GetTabletContextIdFromTablet","rtscom/IRealTimeStylus::GetTabletContextIdFromTablet","tablet.irealtimestylus_gettabletcontextidfromtablet"]
old-location: tablet\irealtimestylus_gettabletcontextidfromtablet.htm
tech.root: tablet
ms.assetid: 9f4cc882-c25f-4862-8b78-4db108d0b5d4
ms.date: 12/05/2018
ms.keywords: 9f4cc882-c25f-4862-8b78-4db108d0b5d4, GetTabletContextIdFromTablet, GetTabletContextIdFromTablet method [Tablet PC], GetTabletContextIdFromTablet method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetTabletContextIdFromTablet method, IRealTimeStylus.GetTabletContextIdFromTablet, IRealTimeStylus::GetTabletContextIdFromTablet, rtscom/IRealTimeStylus::GetTabletContextIdFromTablet, tablet.irealtimestylus_gettabletcontextidfromtablet
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
 - IRealTimeStylus::GetTabletContextIdFromTablet
 - rtscom/IRealTimeStylus::GetTabletContextIdFromTablet
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
 - IRealTimeStylus.GetTabletContextIdFromTablet
---

# IRealTimeStylus::GetTabletContextIdFromTablet


## -description

Retrieves the TabletContextId property that is associated with a given tablet digitizer object.

## -parameters

### -param piTablet [in]

Specifies the tablet object associated with a digitizer for which to get the unique identifier for the tablet context.

### -param ptcid [out, retval]

The unique identifier for the tablet context.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

A digitizer context identifier is specific to an <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object. Two <b>RealTimeStylus Class</b> objects may have different context identifiers for the same digitizer object. A tablet context identifier is valid only while a <b>RealTimeStylus Class</b> object is enabled. If a <b>RealTimeStylus Class</b> object is disabled and then re-enabled, the TCID for each digitizer object might have a different value than it had when the <b>RealTimeStylus Class</b> object was first enabled.

This method can be called even if the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object is not enabled as long as the <b>RealTimeStylus Class</b> has not finished processing data in the queue. This method can be called until the last asynchronous plug-in receives <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-realtimestylusdisabled">IStylusPlugin::RealTimeStylusDisabled Method</a>.


#### Examples

The following C++ example code gets a pointer to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> object and uses that to get the tablet context identifier. Then it displays the names of all the tablets attached to the system in the debug output window.


```cpp
TABLET_CONTEXT_ID* pTcids = NULL;
TABLET_CONTEXT_ID tcid = 0;
ULONG ulTcidCount = 0;
IInkTablet* pInkTablet = NULL;

if (SUCCEEDED(g_pRealTimeStylus->GetAllTabletContextIds(&ulTcidCount, &pTcids)))
{
    TRACE("Got the tablet context ID array.\n");

    // Loop through all the tablets on the system
    for (ULONG i = 0; i < ulTcidCount; i++)
    {
        // Get the tablet from the context ID
        if (SUCCEEDED(g_pRealTimeStylus->GetTabletFromTabletContextId(pTcids[i], &pInkTablet)))
        {
            // Display the name of the tablet in debug output
            BSTR bstrName;
            if (SUCCEEDED(pInkTablet->get_Name(&bstrName)))
            {
                TRACE("The name of tablet %d is %s.\n", i, bstrName);
            }
        }
    }

    // Get the context ID from the tablet
    if (SUCCEEDED(g_pRealTimeStylus->GetTabletContextIdFromTablet(pInkTablet, &tcid)))
    {
        TRACE("The context ID of the tablet is %d\n", tcid);
    }
}

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-gettabletfromtabletcontextid">IRealTimeStylus::GetTabletFromTabletContextId Method</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>