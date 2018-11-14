---
UID: NF:rtscom.IRealTimeStylus.GetAllTabletContextIds
title: IRealTimeStylus::GetAllTabletContextIds
author: windows-sdk-content
description: Retrieves an array containing all of the currently active tablet context identifiers.
old-location: tablet\irealtimestylus_getalltabletcontextids.htm
tech.root: tablet
ms.assetid: 1fac0624-2e1c-44b2-8a11-82b746a18356
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 1fac0624-2e1c-44b2-8a11-82b746a18356, GetAllTabletContextIds, GetAllTabletContextIds method [Tablet PC], GetAllTabletContextIds method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetAllTabletContextIds method, IRealTimeStylus.GetAllTabletContextIds, IRealTimeStylus::GetAllTabletContextIds, rtscom/IRealTimeStylus::GetAllTabletContextIds, tablet.irealtimestylus_getalltabletcontextids
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
 - IRealTimeStylus.GetAllTabletContextIds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rtscom.h
: 
- IRealTimeStylus.GetAllTabletContextIds
: 
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



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



<b>IRealTimeStylus::GetAllTabletContextIds Method</b> method provides access to all the tablet context identifiers that are currently active. This method enables you to get these identifiers directly instead of caching data from <a href="https://msdn.microsoft.com/bd5689c1-32e2-4a37-8dd2-4525b16f4662">IStylusPlugin::RealTimeStylusEnabled Method</a> notifications.

The scope of the TabletContextID property is limited to a given instance of the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>; a Tablet object may have a different unique identifier for each instance of the <b>RealTimeStylus Class</b>.


#### Examples

The following C++ example code gets all the tablet context identifiers and uses the first tablet context identifier to get a pointer to the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a> object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>TABLET_CONTEXT_ID* pTcids = NULL;
TABLET_CONTEXT_ID tcid = 0;
ULONG ulTcidCount = 0;
IInkTablet* pInkTablet = NULL;

if (SUCCEEDED(g_pRealTimeStylus-&gt;GetAllTabletContextIds(&amp;ulTcidCount, &amp;pTcids)))
{
    TRACE("Got the tablet context ID array.\n");

    // Loop through all the tablets on the system
    for (ULONG i = 0; i &lt; ulTcidCount; i++)
    {
        // Get the tablet from the context ID
        if (SUCCEEDED(g_pRealTimeStylus-&gt;GetTabletFromTabletContextId(pTcids[i], &amp;pInkTablet)))
        {
            // Display the name of the tablet in debug output
            BSTR bstrName;
            if (SUCCEEDED(pInkTablet-&gt;get_Name(&amp;bstrName)))
            {
                TRACE("The name of tablet %d is %s.\n", i, bstrName);
            }
        }
    }

    // Get the context ID from the tablet
    if (SUCCEEDED(g_pRealTimeStylus-&gt;GetTabletContextIdFromTablet(pInkTablet, &amp;tcid)))
    {
        TRACE("The context ID of the tablet is %d\n", tcid);
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/be736eaf-8632-4e71-b1d8-c851a9d417e5">IRealTimeStylus::GetTabletFromTabletContextId Method</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

