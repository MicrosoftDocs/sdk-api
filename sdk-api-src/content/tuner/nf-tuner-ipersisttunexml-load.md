---
UID: NF:tuner.IPersistTuneXml.Load
title: IPersistTuneXml::Load (tuner.h)
description: Deserializes a tuning model object from an XML node.
helpviewer_keywords: ["IPersistTuneXml interface [Microsoft TV Technologies]","Load method","IPersistTuneXml.Load","IPersistTuneXml::Load","Load","Load method [Microsoft TV Technologies]","Load method [Microsoft TV Technologies]","IPersistTuneXml interface","mstv.ipersisttunexml_load","tuner/IPersistTuneXml::Load"]
old-location: mstv\ipersisttunexml_load.htm
tech.root: mstv
ms.assetid: afbfb4da-ac61-496b-9383-05c312bbfc2c
ms.date: 12/05/2018
ms.keywords: IPersistTuneXml interface [Microsoft TV Technologies],Load method, IPersistTuneXml.Load, IPersistTuneXml::Load, Load, Load method [Microsoft TV Technologies], Load method [Microsoft TV Technologies],IPersistTuneXml interface, mstv.ipersisttunexml_load, tuner/IPersistTuneXml::Load
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
 - IPersistTuneXml::Load
 - tuner/IPersistTuneXml::Load
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
 - IPersistTuneXml.Load
---

# IPersistTuneXml::Load


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Deserializes a tuning model object from an XML node.

## -parameters

### -param varValue [in]

XML node used to deserialize the object. This parameter can be either a <b>BSTR</b> object or an <b>IXMLDOMNode</b> object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ipersisttunexml">IPersistTuneXml</a>