---
UID: NN:tuner.IPersistTuneXmlUtility
title: IPersistTuneXmlUtility (tuner.h)
author: windows-sdk-content
description: Defines utility methods for deserializing XML tuning requests to objects that expose their IUnknown interfaces.
old-location: mstv\ipersisttunexmlutility.htm
tech.root: mstv
ms.assetid: aa03015f-094f-499f-99fb-2e15ead74f15
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPersistTuneXmlUtility, IPersistTuneXmlUtility interface [Microsoft TV Technologies], IPersistTuneXmlUtility interface [Microsoft TV Technologies],described, mstv.ipersisttunexmlutility, tuner/IPersistTuneXmlUtility
ms.topic: interface
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
 - IPersistTuneXmlUtility
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPersistTuneXmlUtility interface


## -description


Defines utility methods for deserializing XML tuning requests to objects that expose their <b>IUnknown</b> interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistTuneXmlUtility</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPersistTuneXmlUtility</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistTuneXmlUtility</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ipersisttunexmlutility-deserialize">Deserialize</a>
</td>
<td align="left" width="63%">
Constructs and returns an object that initializes itself by using the XML node passed as a <b>VARIANT</b> parameter to the method. The returned object exposes its <b>IUnknown</b> interface so that other objects can query it.
    
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IPersistTuneXmlUtility)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

