---
UID: NF:tuner.IPersistTuneXmlUtility2.Serialize
title: IPersistTuneXmlUtility2::Serialize (tuner.h)
description: Serializes a tuning request to an XML tuning request string.
helpviewer_keywords: ["IPersistTuneXmlUtility2 interface [Microsoft TV Technologies]","Serialize method","IPersistTuneXmlUtility2.Serialize","IPersistTuneXmlUtility2::Serialize","Serialize","Serialize method [Microsoft TV Technologies]","Serialize method [Microsoft TV Technologies]","IPersistTuneXmlUtility2 interface","mstv.ipersisttunexmlutility2_serialize","tuner/IPersistTuneXmlUtility2::Serialize"]
old-location: mstv\ipersisttunexmlutility2_serialize.htm
tech.root: mstv
ms.assetid: 463ddd94-5eb1-4553-a31d-0a06326eceec
ms.date: 12/05/2018
ms.keywords: IPersistTuneXmlUtility2 interface [Microsoft TV Technologies],Serialize method, IPersistTuneXmlUtility2.Serialize, IPersistTuneXmlUtility2::Serialize, Serialize, Serialize method [Microsoft TV Technologies], Serialize method [Microsoft TV Technologies],IPersistTuneXmlUtility2 interface, mstv.ipersisttunexmlutility2_serialize, tuner/IPersistTuneXmlUtility2::Serialize
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
 - IPersistTuneXmlUtility2::Serialize
 - tuner/IPersistTuneXmlUtility2::Serialize
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
 - IPersistTuneXmlUtility2.Serialize
---

# IPersistTuneXmlUtility2::Serialize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Serializes a tuning request to an XML tuning request string.

## -parameters

### -param piTuneRequest [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-itunerequestinfo">ITuneRequest</a> interface for the tuning request object that is serialized.

### -param pString

Pointer to a buffer that receives the XML tuning request string. The caller is responsible for releasing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ipersisttunexmlutility2">IPersistTuneXmlUtility2</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ipersisttunexmlutility-deserialize">IPersistTuneXmlUtility::Deserialize</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-itunerequestinfo">ITuneRequest</a>