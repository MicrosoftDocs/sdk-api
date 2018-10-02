---
UID: NN:tuner.IPersistTuneXml
title: IPersistTuneXml
author: windows-sdk-content
description: Implements methods for serializing tuning model objects. All serializable tuning model objects are required to implement this interface.
old-location: mstv\ipersisttunexml.htm
tech.root: MSTV
ms.assetid: 2e08f727-9ffe-435b-9eca-4e9867fe410b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPersistTuneXml, IPersistTuneXml interface [Microsoft TV Technologies], IPersistTuneXml interface [Microsoft TV Technologies],described, mstv.ipersisttunexml, tuner/IPersistTuneXml
ms.prod: windows
ms.technology: windows-sdk
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
 - IPersistTuneXml
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistTuneXml interface


## -description


Implements methods for serializing tuning model objects. All serializable tuning model objects are required to implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistTuneXml</b> interface inherits from <b>IPersist</b>. <b>IPersistTuneXml</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistTuneXml</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75485d59-118c-4098-974b-40f7a36dbd91">InitNew</a>
</td>
<td align="left" width="63%">
Not implemented in the current release.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afbfb4da-ac61-496b-9383-05c312bbfc2c">Load</a>
</td>
<td align="left" width="63%">
Deserializes a tuning model object from an XML node.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5813966a-6053-43ce-9b92-e9552d9acdec">Save</a>
</td>
<td align="left" width="63%">
Serializes a tuning model object to an XML node.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IPersistTuneXml)</code>.



