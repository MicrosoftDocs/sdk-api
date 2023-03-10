---
UID: NF:rtscom.IRealTimeStylus.SetAllTabletsMode
title: IRealTimeStylus::SetAllTabletsMode (rtscom.h)
description: Sets the mode for the RealTimeStylus Class object to collect data from all digitizers.
helpviewer_keywords: ["IRealTimeStylus interface [Tablet PC]","SetAllTabletsMode method","IRealTimeStylus.SetAllTabletsMode","IRealTimeStylus::SetAllTabletsMode","SetAllTabletsMode","SetAllTabletsMode method [Tablet PC]","SetAllTabletsMode method [Tablet PC]","IRealTimeStylus interface","cb8b2a17-68b9-482b-b212-ad129522ff2e","rtscom/IRealTimeStylus::SetAllTabletsMode","tablet.irealtimestylus_setalltabletsmode"]
old-location: tablet\irealtimestylus_setalltabletsmode.htm
tech.root: tablet
ms.assetid: cb8b2a17-68b9-482b-b212-ad129522ff2e
ms.date: 12/05/2018
ms.keywords: IRealTimeStylus interface [Tablet PC],SetAllTabletsMode method, IRealTimeStylus.SetAllTabletsMode, IRealTimeStylus::SetAllTabletsMode, SetAllTabletsMode, SetAllTabletsMode method [Tablet PC], SetAllTabletsMode method [Tablet PC],IRealTimeStylus interface, cb8b2a17-68b9-482b-b212-ad129522ff2e, rtscom/IRealTimeStylus::SetAllTabletsMode, tablet.irealtimestylus_setalltabletsmode
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
 - IRealTimeStylus::SetAllTabletsMode
 - rtscom/IRealTimeStylus::SetAllTabletsMode
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
 - IRealTimeStylus.SetAllTabletsMode
---

# IRealTimeStylus::SetAllTabletsMode


## -description

Sets the mode for the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object to collect data from all digitizers.

## -parameters

### -param fUseMouseForInput [in]

<b>TRUE</b> for both the mouse and stylus to be used for input; <b>FALSE</b> for the mouse not to be used as input.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

This method enables the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object to collect stylus events from any tablet attached to the Tablet PC. The <i>fUseMouseForInput</i> parameter specifies whether the mouse device, as well as the stylus, can be used for input.

If <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setsingletabletmode">IRealTimeStylus::SetSingleTabletMode Method</a> () was initially called and <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object is enabled, this call is invalid and TPC_E_INVALID_MODE HRESULT is returned.

<div class="alert"><b>Note</b>  The <b>IRealTimeStylus::SetAllTabletsMode Method</b> method will fail if the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> is enabled. On Microsoft Windows XP, this method will return <b>S_OK</b> but will have no effect. On Windows Vista, this method will return <b>E_INVALID_MODE</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-gettablet">IRealTimeStylus::GetTablet Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setsingletabletmode">IRealTimeStylus::SetSingleTabletMode Method</a>



<b>RealTimeStylus Class</b>