---
UID: NF:rtscom.IRealTimeStylus.SetSingleTabletMode
title: IRealTimeStylus::SetSingleTabletMode (rtscom.h)
description: Modifies the mode for RealTimeStylus Class (RTS) object to collect input from only one tablet object representing a digitizer attached to the Tablet PC. Stylus input from other digitizers is ignored by the RealTimeStylus.
helpviewer_keywords: ["7f3645fd-cb1e-4bd5-a995-d70197c61afc","IRealTimeStylus interface [Tablet PC]","SetSingleTabletMode method","IRealTimeStylus.SetSingleTabletMode","IRealTimeStylus::SetSingleTabletMode","SetSingleTabletMode","SetSingleTabletMode method [Tablet PC]","SetSingleTabletMode method [Tablet PC]","IRealTimeStylus interface","rtscom/IRealTimeStylus::SetSingleTabletMode","tablet.irealtimestylus_setsingletabletmode"]
old-location: tablet\irealtimestylus_setsingletabletmode.htm
tech.root: tablet
ms.assetid: 7f3645fd-cb1e-4bd5-a995-d70197c61afc
ms.date: 12/05/2018
ms.keywords: 7f3645fd-cb1e-4bd5-a995-d70197c61afc, IRealTimeStylus interface [Tablet PC],SetSingleTabletMode method, IRealTimeStylus.SetSingleTabletMode, IRealTimeStylus::SetSingleTabletMode, SetSingleTabletMode, SetSingleTabletMode method [Tablet PC], SetSingleTabletMode method [Tablet PC],IRealTimeStylus interface, rtscom/IRealTimeStylus::SetSingleTabletMode, tablet.irealtimestylus_setsingletabletmode
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
 - IRealTimeStylus::SetSingleTabletMode
 - rtscom/IRealTimeStylus::SetSingleTabletMode
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
 - IRealTimeStylus.SetSingleTabletMode
---

# IRealTimeStylus::SetSingleTabletMode


## -description

Modifies the mode for <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> (RTS) object to collect input from only one tablet object representing a digitizer attached to the Tablet PC. Stylus input from other digitizers is ignored by the RealTimeStylus.

## -parameters

### -param piTablet [in]

 The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a> object that represents the digitizer device attached to the Tablet PC.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

A <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> can be set to one of two tablet-related modes:

<ul>
<li>All tablets mode (default)</li>
<li>Single tablet mode</li>
</ul>
If <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setalltabletsmode">IRealTimeStylus::SetAllTabletsMode Method</a> () was initially called and the RealTimeStylus is enabled, the TPC_E_INVALID_MODE HRESULT is returned.


#### Examples

The following C++ example code sets a <a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a> object, <code>g_pRealTimeStylus</code>, to single tablet mode so it can get the tablet and retrieve its plug-and-play identifier. Then it sets the <b>IRealTimeStylus</b> object back to all tablets mode.


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

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="/windows/desktop/tablet/realtimestylus-reference">RealTimeStylus Reference</a>