---
UID: NF:tuner.IPersistTuneXml.Save
title: IPersistTuneXml::Save (tuner.h)
description: Serializes a tuning model object to an XML node.
helpviewer_keywords: ["IPersistTuneXml interface [Microsoft TV Technologies]","Save method","IPersistTuneXml.Save","IPersistTuneXml::Save","Save","Save method [Microsoft TV Technologies]","Save method [Microsoft TV Technologies]","IPersistTuneXml interface","mstv.ipersisttunexml_save","tuner/IPersistTuneXml::Save"]
old-location: mstv\ipersisttunexml_save.htm
tech.root: mstv
ms.assetid: 5813966a-6053-43ce-9b92-e9552d9acdec
ms.date: 12/05/2018
ms.keywords: IPersistTuneXml interface [Microsoft TV Technologies],Save method, IPersistTuneXml.Save, IPersistTuneXml::Save, Save, Save method [Microsoft TV Technologies], Save method [Microsoft TV Technologies],IPersistTuneXml interface, mstv.ipersisttunexml_save, tuner/IPersistTuneXml::Save
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
 - IPersistTuneXml::Save
 - tuner/IPersistTuneXml::Save
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
 - IPersistTuneXml.Save
---

# IPersistTuneXml::Save


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Serializes a tuning model object to an XML node.

## -parameters

### -param pvarFragment [out]

Pointer to an <b>IXMLDOMNode</b> object that gets the data for the tuning model object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ipersisttunexml">IPersistTuneXml</a>