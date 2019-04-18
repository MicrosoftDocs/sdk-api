---
UID: NF:rtscom.IRealTimeStylus.SetSingleTabletMode
title: IRealTimeStylus::SetSingleTabletMode (rtscom.h)
author: windows-sdk-content
description: Modifies the mode for RealTimeStylus Class (RTS) object to collect input from only one tablet object representing a digitizer attached to the Tablet PC. Stylus input from other digitizers is ignored by the RealTimeStylus.
old-location: tablet\irealtimestylus_setsingletabletmode.htm
tech.root: tablet
ms.assetid: 7f3645fd-cb1e-4bd5-a995-d70197c61afc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 7f3645fd-cb1e-4bd5-a995-d70197c61afc, IRealTimeStylus interface [Tablet PC],SetSingleTabletMode method, IRealTimeStylus.SetSingleTabletMode, IRealTimeStylus::SetSingleTabletMode, SetSingleTabletMode, SetSingleTabletMode method [Tablet PC], SetSingleTabletMode method [Tablet PC],IRealTimeStylus interface, rtscom/IRealTimeStylus::SetSingleTabletMode, tablet.irealtimestylus_setsingletabletmode
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
 - IRealTimeStylus.SetSingleTabletMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRealTimeStylus::SetSingleTabletMode


## -description



Modifies the mode for <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> (RTS) object to collect input from only one tablet object representing a digitizer attached to the Tablet PC. Stylus input from other digitizers is ignored by the RealTimeStylus.




## -parameters




### -param piTablet [in]

 The <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a> object that represents the digitizer device attached to the Tablet PC.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



A <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> can be set to one of two tablet-related modes:

<ul>
<li>All tablets mode (default)</li>
<li>Single tablet mode</li>
</ul>
If <a href="https://msdn.microsoft.com/cb8b2a17-68b9-482b-b212-ad129522ff2e">IRealTimeStylus::SetAllTabletsMode Method</a> () was initially called and the RealTimeStylus is enabled, the TPC_E_INVALID_MODE HRESULT is returned.


#### Examples

The following C++ example code sets a <a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a> object, <code>g_pRealTimeStylus</code>, to single tablet mode so it can get the tablet and retrieve its plug-and-play identifier. Then it sets the <b>IRealTimeStylus</b> object back to all tablets mode.


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




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/a239b53c-7fc9-4211-962a-6cfbe0be4e4c">RealTimeStylus Reference</a>
 

 

