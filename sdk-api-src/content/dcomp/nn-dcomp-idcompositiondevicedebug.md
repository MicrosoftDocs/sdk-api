---
UID: NN:dcomp.IDCompositionDeviceDebug
title: IDCompositionDeviceDebug (dcomp.h)
description: Provides access to rendering features that help with application debugging and performance tuning. This interface can be queried from the DirectComposition device interface.helpviewer_keywords: ["IDCompositionDeviceDebug","IDCompositionDeviceDebug interface [DirectComposition]","IDCompositionDeviceDebug interface [DirectComposition]","described","dcomp/IDCompositionDeviceDebug","directcomp.idcompositiondevicedebug"]
old-location: directcomp\idcompositiondevicedebug.htm
tech.root: directcomp
ms.assetid: B8D17570-9729-45DB-99E1-A2EBBDAA5996
ms.date: 12/05/2018
ms.keywords: IDCompositionDeviceDebug, IDCompositionDeviceDebug interface [DirectComposition], IDCompositionDeviceDebug interface [DirectComposition],described, dcomp/IDCompositionDeviceDebug, directcomp.idcompositiondevicedebug
f1_keywords:
- dcomp/IDCompositionDeviceDebug
dev_langs:
- c++
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dcomp.h
api_name:
- IDCompositionDeviceDebug
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDeviceDebug interface


## -description


Provides access to rendering features that help with application debugging and performance tuning. This interface can be queried from the DirectComposition device interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionDeviceDebug</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDCompositionDeviceDebug</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionDeviceDebug</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevicedebug-disabledebugcounters">DisableDebugCounters</a>
</td>
<td align="left" width="63%">
Disables display of performance debugging counters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevicedebug-enabledebugcounters">EnableDebugCounters</a>
</td>
<td align="left" width="63%">
Enables display of performance debugging counters.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondesktopdevice">IDCompositionDesktopDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisualdebug">IDCompositionVisualDebug</a>
 

 

