---
UID: NN:tuner.IDVBTuningSpace
title: IDVBTuningSpace (tuner.h)

description: The IDVBTuningSpace interface is implemented on the DVBTuningSpace object.Note  New applications should use the IDVBTuningSpace2 interface, which inherits IDVBTuningSpace and adds additional methods. .
old-location: mstv\idvbtuningspace.htm
tech.root: mstv
ms.assetid: fba3c7f3-61f8-4704-8068-cb1d3171345a

ms.date: 12/05/2018
ms.keywords: IDVBTuningSpace, IDVBTuningSpace interface [Microsoft TV Technologies], IDVBTuningSpace interface [Microsoft TV Technologies],described, IDVBTuningSpaceInterface, mstv.idvbtuningspace, tuner/IDVBTuningSpace
ms.topic: interface
f1_keywords: 
 - "tuner/IDVBTuningSpace"
dev_langs:
 - c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
 - tuner.h
api_name:
 - IDVBTuningSpace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVBTuningSpace interface


## -description



The <b>IDVBTuningSpace</b> interface is implemented on the DVBTuningSpace object.

<div class="alert"><b>Note</b>  New applications should use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtuningspace2">IDVBTuningSpace2</a> interface, which inherits <b>IDVBTuningSpace</b> and adds additional methods.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVBTuningSpace</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a>. <b>IDVBTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVBTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtuningspace-get_systemtype">get_SystemType</a>
</td>
<td align="left" width="63%">
Retrieves the DVB system type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtuningspace-put_systemtype">put_SystemType</a>
</td>
<td align="left" width="63%">
Sets the DVB system type.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBTuningSpace)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

