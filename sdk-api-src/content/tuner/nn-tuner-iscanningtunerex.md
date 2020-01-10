---
UID: NN:tuner.IScanningTunerEx
title: IScanningTunerEx (tuner.h)
description: This topic applies to Windows Vista.
old-location: mstv\iscanningtunerex.htm
tech.root: mstv
ms.assetid: 3f89173a-d24b-400c-a229-28efb7a703be
ms.date: 12/05/2018
ms.keywords: IScanningTunerEx, IScanningTunerEx interface [Microsoft TV Technologies], IScanningTunerEx interface [Microsoft TV Technologies],described, IScanningTunerExInterface, mstv.iscanningtunerex, tuner/IScanningTunerEx
f1_keywords:
- tuner/IScanningTunerEx
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
- Tuner.h
api_name:
- IScanningTunerEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IScanningTunerEx interface


## -description



This topic applies to Windows Vista.
        

The <b>IScanningTunerEx</b> interface is an extended version of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner</a> and is exposed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-network-provider-filter">BDA Network Provider</a> filter. It inherits from <b>IScanningTuner</b> and permits direct control of a tuner that supports searching for valid programming. The client must provide a valid tuning space (using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_tuningspace">ITuner::put_TuningSpace</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_tunerequest">ITuner::put_TuneRequest</a>) before calling any of the methods in this interface. This interface is meant to be used in conjunction with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ibroadcastevent">IBroadcastEvent</a> outbound interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScanningTunerEx</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner</a>. <b>IScanningTunerEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IScanningTunerEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-getcurrentlocator">GetCurrentLocator</a>
</td>
<td align="left" width="63%">
Retrieves the current locator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-getcurrenttunerstandardcapability">GetCurrentTunerStandardCapability</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's capabilities for a specified broadcast standard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-gettunerscanningcapability">GetTunerScanningCapability</a>
</td>
<td align="left" width="63%">
Retrieves the set of broadcast standards supported by the tuner and the tuner's scanning capability.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-gettunerstatus">GetTunerStatus</a>
</td>
<td align="left" width="63%">
Returns the current status of the most recent call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-performexhaustivescan">PerformExhaustiveScan</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-performexhaustivescan">PerformExhaustiveScan</a>
</td>
<td align="left" width="63%">
Scans a range of frequencies until the tuner locks onto a signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-resumecurrentscan">ResumeCurrentScan</a>
</td>
<td align="left" width="63%">
Resumes scanning the range of frequencies specified in <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-performexhaustivescan">PerformExhaustiveScan</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-setscansignaltypefilter">SetScanSignalTypeFilter</a>
</td>
<td align="left" width="63%">
Specifies the type of signal for which to scan.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-terminatecurrentscan">TerminateCurrentScan</a>
</td>
<td align="left" width="63%">
Interrupts the current scan, if a scan is in progress.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IScanningTunerEx)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner</a>
 

 

