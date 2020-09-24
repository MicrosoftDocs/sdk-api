---
UID: NF:rtscom.IRealTimeStylus.GetAllTabletContextIds
title: IRealTimeStylus::GetAllTabletContextIds (rtscom.h)
description: Retrieves an array containing all of the currently active tablet context identifiers.
helpviewer_keywords: ["1fac0624-2e1c-44b2-8a11-82b746a18356","GetAllTabletContextIds","GetAllTabletContextIds method [Tablet PC]","GetAllTabletContextIds method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","GetAllTabletContextIds method","IRealTimeStylus.GetAllTabletContextIds","IRealTimeStylus::GetAllTabletContextIds","rtscom/IRealTimeStylus::GetAllTabletContextIds","tablet.irealtimestylus_getalltabletcontextids"]
old-location: tablet\irealtimestylus_getalltabletcontextids.htm
tech.root: tablet
ms.assetid: 1fac0624-2e1c-44b2-8a11-82b746a18356
ms.date: 12/05/2018
ms.keywords: 1fac0624-2e1c-44b2-8a11-82b746a18356, GetAllTabletContextIds, GetAllTabletContextIds method [Tablet PC], GetAllTabletContextIds method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetAllTabletContextIds method, IRealTimeStylus.GetAllTabletContextIds, IRealTimeStylus::GetAllTabletContextIds, rtscom/IRealTimeStylus::GetAllTabletContextIds, tablet.irealtimestylus_getalltabletcontextids
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
 - IRealTimeStylus::GetAllTabletContextIds
 - rtscom/IRealTimeStylus::GetAllTabletContextIds
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
 - IRealTimeStylus.GetAllTabletContextIds
---

# IRealTimeStylus::GetAllTabletContextIds


## -description

Retrieves an array containing all of the currently active tablet context identifiers.

## -parameters

### -param pcTcidCount [in, out]

The number of tablet context identifiers.

### -param ppTcids [out]

Pointer to the array of tablet context identifiers

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

<b>IRealTimeStylus::GetAllTabletContextIds Method</b> method provides access to all the tablet context identifiers that are currently active. This method enables you to get these identifiers directly instead of caching data from <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-realtimestylusenabled">IStylusPlugin::RealTimeStylusEnabled Method</a> notifications.

The scope of the TabletContextID property is limited to a given instance of the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>; a Tablet object may have a different unique identifier for each instance of the <b>RealTimeStylus Class</b>.


#### Examples

The following C++ example code gets all the tablet context identifiers and uses the first tablet context identifier to get a pointer to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a> object.


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