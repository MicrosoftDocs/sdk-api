---
UID: NF:tuner.IPersistTuneXml.Save
title: IPersistTuneXml::Save (tuner.h)
author: windows-sdk-content
description: Serializes a tuning model object to an XML node.
old-location: mstv\ipersisttunexml_save.htm
tech.root: mstv
ms.assetid: 5813966a-6053-43ce-9b92-e9552d9acdec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPersistTuneXml interface [Microsoft TV Technologies],Save method, IPersistTuneXml.Save, IPersistTuneXml::Save, Save, Save method [Microsoft TV Technologies], Save method [Microsoft TV Technologies],IPersistTuneXml interface, mstv.ipersisttunexml_save, tuner/IPersistTuneXml::Save
ms.topic: method
f1_keywords: 
 - "tuner/IPersistTuneXml.Save"
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
 - IPersistTuneXml.Save
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPersistTuneXml::Save


## -description


Serializes a tuning model object to an XML node.
          


## -parameters




### -param pvarFragment [out]

Pointer to an <b>IXMLDOMNode</b> object that gets the data for the tuning model object.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ipersisttunexml">IPersistTuneXml</a>
 

 

