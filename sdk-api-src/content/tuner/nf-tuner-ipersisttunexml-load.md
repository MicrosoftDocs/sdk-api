---
UID: NF:tuner.IPersistTuneXml.Load
title: IPersistTuneXml::Load (tuner.h)
description: Deserializes a tuning model object from an XML node.
old-location: mstv\ipersisttunexml_load.htm
tech.root: mstv
ms.assetid: afbfb4da-ac61-496b-9383-05c312bbfc2c
ms.date: 12/05/2018
ms.keywords: IPersistTuneXml interface [Microsoft TV Technologies],Load method, IPersistTuneXml.Load, IPersistTuneXml::Load, Load, Load method [Microsoft TV Technologies], Load method [Microsoft TV Technologies],IPersistTuneXml interface, mstv.ipersisttunexml_load, tuner/IPersistTuneXml::Load
ms.topic: method
f1_keywords:
- tuner/IPersistTuneXml.Load
dev_langs:
- c++
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
- IPersistTuneXml.Load
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPersistTuneXml::Load


## -description


Deserializes a tuning model object from an XML node. 


## -parameters




### -param varValue [in]

XML node used to deserialize the object. This parameter can be either a <b>BSTR</b> object or an <b>IXMLDOMNode</b> object.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ipersisttunexml">IPersistTuneXml</a>
 

 

