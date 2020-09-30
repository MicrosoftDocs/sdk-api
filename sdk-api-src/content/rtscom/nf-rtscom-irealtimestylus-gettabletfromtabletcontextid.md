---
UID: NF:rtscom.IRealTimeStylus.GetTabletFromTabletContextId
title: IRealTimeStylus::GetTabletFromTabletContextId (rtscom.h)
description: Retrieves an IInkTablet Interface for a specified tablet context.
helpviewer_keywords: ["GetTabletFromTabletContextId","GetTabletFromTabletContextId method [Tablet PC]","GetTabletFromTabletContextId method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","GetTabletFromTabletContextId method","IRealTimeStylus.GetTabletFromTabletContextId","IRealTimeStylus::GetTabletFromTabletContextId","be736eaf-8632-4e71-b1d8-c851a9d417e5","rtscom/IRealTimeStylus::GetTabletFromTabletContextId","tablet.irealtimestylus_gettabletfromtabletcontextid"]
old-location: tablet\irealtimestylus_gettabletfromtabletcontextid.htm
tech.root: tablet
ms.assetid: be736eaf-8632-4e71-b1d8-c851a9d417e5
ms.date: 12/05/2018
ms.keywords: GetTabletFromTabletContextId, GetTabletFromTabletContextId method [Tablet PC], GetTabletFromTabletContextId method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetTabletFromTabletContextId method, IRealTimeStylus.GetTabletFromTabletContextId, IRealTimeStylus::GetTabletFromTabletContextId, be736eaf-8632-4e71-b1d8-c851a9d417e5, rtscom/IRealTimeStylus::GetTabletFromTabletContextId, tablet.irealtimestylus_gettabletfromtabletcontextid
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
 - IRealTimeStylus::GetTabletFromTabletContextId
 - rtscom/IRealTimeStylus::GetTabletFromTabletContextId
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
 - IRealTimeStylus.GetTabletFromTabletContextId
---

# IRealTimeStylus::GetTabletFromTabletContextId


## -description

Retrieves an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a> for a specified tablet context.

## -parameters

### -param tcid [in]

Specifies the unique identifier for the tablet context.

### -param ppiTablet [out, retval]

A pointer to the digitizer object specified by the tablet context identifier.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

A tablet context identifier is specific to a <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object. Two <b>RealTimeStylus Class</b> objects can have different context identifiers for the same tablet object. A tablet context identifier is only valid while a <b>RealTimeStylus Class</b> object is enabled. If a <b>RealTimeStylus Class</b> object is disabled and then re-enabled, the tablet context identifier for each tablet object may have a different value than when the <b>RealTimeStylus Class</b> object was first enabled.

This method can be called even if <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-get_enabled">IRealTimeStylus::Enabled Property</a> returns <b>false</b> as long as the <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-realtimestylusdisabled">IStylusPlugin::RealTimeStylusDisabled Method</a> has not finished processing data in the queue. This method can be called until the last asynchronous plug-in receives <b>IStylusPlugin::RealTimeStylusDisabled Method</b>.


#### Examples

The following C++ example code uses the tablet context identifier to get a pointer to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a> object.


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



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-gettabletcontextidfromtablet">IRealTimeStylus::GetTabletContextIdFromTablet Method</a>



<b>RealTimeStylus Class</b>