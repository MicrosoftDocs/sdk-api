---
UID: NN:tuner.IPersistTuneXml
title: IPersistTuneXml (tuner.h)
description: Implements methods for serializing tuning model objects. All serializable tuning model objects are required to implement this interface.
helpviewer_keywords: ["IPersistTuneXml","IPersistTuneXml interface [Microsoft TV Technologies]","IPersistTuneXml interface [Microsoft TV Technologies]","described","mstv.ipersisttunexml","tuner/IPersistTuneXml"]
old-location: mstv\ipersisttunexml.htm
tech.root: mstv
ms.assetid: 2e08f727-9ffe-435b-9eca-4e9867fe410b
ms.date: 12/05/2018
ms.keywords: IPersistTuneXml, IPersistTuneXml interface [Microsoft TV Technologies], IPersistTuneXml interface [Microsoft TV Technologies],described, mstv.ipersisttunexml, tuner/IPersistTuneXml
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistTuneXml
 - tuner/IPersistTuneXml
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IPersistTuneXml
---

# IPersistTuneXml interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements methods for serializing tuning model objects. All serializable tuning model objects are required to implement this interface.

## -inheritance

The <b>IPersistTuneXml</b> interface inherits from <b>IPersist</b>. <b>IPersistTuneXml</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IPersistTuneXml)</code>.
