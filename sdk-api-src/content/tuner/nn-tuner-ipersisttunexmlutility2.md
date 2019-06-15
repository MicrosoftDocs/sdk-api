---
UID: NN:tuner.IPersistTuneXmlUtility2
title: IPersistTuneXmlUtility2 (tuner.h)
author: windows-sdk-content
description: Defines utility methods for serializing tuning requests (objects that implement the ITuneRequest interface) to XML tuning request strings.
old-location: mstv\ipersisttunexmlutility2.htm
tech.root: mstv
ms.assetid: d909d505-2ae9-4488-b4c1-42ca32661bf3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPersistTuneXmlUtility2, IPersistTuneXmlUtility2 interface [Microsoft TV Technologies], IPersistTuneXmlUtility2 interface [Microsoft TV Technologies],described, mstv.ipersisttunexmlutility2, tuner/IPersistTuneXmlUtility2
ms.topic: interface
f1_keywords: ["tuner/IPersistTuneXmlUtility2"]
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IPersistTuneXmlUtility2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPersistTuneXmlUtility2 interface


## -description


Defines utility methods for serializing tuning requests (objects that implement the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> interface) to XML tuning request strings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistTuneXmlUtility2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ipersisttunexmlutility">IPersistTuneXmlUtility</a>. <b>IPersistTuneXmlUtility2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistTuneXmlUtility2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ipersisttunexmlutility2-serialize">Serialize</a>
</td>
<td align="left" width="63%">
Constructs and returns an object that serializes a tuning request to an XML node.
    
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IPersistTuneXmlUtility2)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ipersisttunexmlutility">IPersistTuneXmlUtility</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

