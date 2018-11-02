---
UID: NF:rtscom.IRealTimeStylus.GetTabletContextIdFromTablet
title: IRealTimeStylus::GetTabletContextIdFromTablet
author: windows-sdk-content
description: Retrieves the TabletContextId property that is associated with a given tablet digitizer object.
old-location: tablet\irealtimestylus_gettabletcontextidfromtablet.htm
tech.root: tablet
ms.assetid: 9f4cc882-c25f-4862-8b78-4db108d0b5d4
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 9f4cc882-c25f-4862-8b78-4db108d0b5d4, GetTabletContextIdFromTablet, GetTabletContextIdFromTablet method [Tablet PC], GetTabletContextIdFromTablet method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetTabletContextIdFromTablet method, IRealTimeStylus.GetTabletContextIdFromTablet, IRealTimeStylus::GetTabletContextIdFromTablet, rtscom/IRealTimeStylus::GetTabletContextIdFromTablet, tablet.irealtimestylus_gettabletcontextidfromtablet
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IRealTimeStylus.GetTabletContextIdFromTablet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



A digitizer context identifier is specific to an <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object. Two <b>RealTimeStylus Class</b> objects may have different context identifiers for the same digitizer object. A tablet context identifier is valid only while a <b>RealTimeStylus Class</b> object is enabled. If a <b>RealTimeStylus Class</b> object is disabled and then re-enabled, the TCID for each digitizer object might have a different value than it had when the <b>RealTimeStylus Class</b> object was first enabled.

This method can be called even if the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object is not enabled as long as the <b>RealTimeStylus Class</b> has not finished processing data in the queue. This method can be called until the last asynchronous plug-in receives <a href="https://msdn.microsoft.com/62425c21-62fb-4a29-b024-8d5dc237b430">IStylusPlugin::RealTimeStylusDisabled Method</a>.


#### Examples

The following C++ example code gets a pointer to the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object and uses that to get the tablet context identifier. Then it displays the names of all the tablets attached to the system in the debug output window.


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




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/be736eaf-8632-4e71-b1d8-c851a9d417e5">IRealTimeStylus::GetTabletFromTabletContextId Method</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

